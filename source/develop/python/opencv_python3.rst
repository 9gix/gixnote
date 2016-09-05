Setup OpenCV for Python 3
#########################

1. Install `Python 3`_ (default Python is x86)
2. Install `Visual C++ 2015 Redistributable package`_  (use the x86 for default python)
3. Install `OpenCV`_

   ``pip install opencv_python-3.1.0-cp35m-win32.whl`` (use win32 for default python)

Done:

>>> import cv2
>>> print(cv2.__version__)
    
* For `OpenCV 3.1 Docs`_
* For `OpenCV 2.4 Docs`_

    FYI: Why python 3.x binds opencv 3.x but import cv2? 
    ANS: cv2 is a prefix for C++ API, whereas cv is a prefix for C API

.. _Python 3: https://www.python.org/downloads/
.. _Visual C++ 2015 Redistributable package: https://www.microsoft.com/en-sg/download/confirmation.aspx?id=48145
.. _OpenCV: http://www.lfd.uci.edu/~gohlke/pythonlibs/#opencv
.. _OpenCV 2.4 Docs: http://docs.opencv.org/2.4/
.. _OpenCV 3.1 Docs: http://docs.opencv.org/3.1.0/index.html
