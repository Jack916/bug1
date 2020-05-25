# bug1
I find a bug ,can't figure out. I do it anaconda ,i hope get a matrix  equation,  a ,b of ax=b  , and using bicgstab  to solve 
AttributeError                            Traceback (most recent call last)
<ipython-input-31-611df0af4a77> in <module>
     15 # Create the simulation
     16 prob.pair(survey)
---> 17 A=prob.getA(freq)

~\anacoda\lib\site-packages\SimPEG\EM\FDEM\ProblemFDEM.py in getA(self, freq)
    257 
    258         MfMui = self.MfMui
--> 259         MeSigma = self.MeSigma
    260         C = self.mesh.edgeCurl
    261 

~\anacoda\lib\site-packages\SimPEG\EM\Base.py in MeSigma(self)
    343         """
    344         if getattr(self, '_MeSigma', None) is None:
--> 345             self._MeSigma = self.mesh.getEdgeInnerProduct(self.sigma)
    346         return self._MeSigma
    347 

~\anacoda\lib\site-packages\SimPEG\Props.py in fget(self)
    209                 raise AttributeError(
    210                     'A `model` is required for physical property {}'.format(
--> 211                         scope.name
    212                     )
    213                 )

AttributeError: A `model` is required for physical property sigma
