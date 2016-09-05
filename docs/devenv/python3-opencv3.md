# Setup OpenCV for Python 3 in Windows

1. Install [Python 3][1] (default Python is x86)
2. Install [Visual C++ 2015 Redistributable package][2]  (use the x86 for default python)
3. Install [OpenCV Windows Binary][3] (use win32 for default python)

        pip install opencv_python-3.1.0-cp35m-win32.whl

4. Verify:

        import cv2
        print(cv2.__version__)
    
5. Read Docs:

    * For [OpenCV 2.4 Docs][4]
    * For [OpenCV 3.1 Docs][5]

> Q: Why Python 3.x which binds OpenCV 3.x but still import cv2? 

> A: cv2 is a prefix for C++ API, whereas cv is a prefix for C API

[1]: https://www.python.org/downloads/
[2]: https://www.microsoft.com/en-sg/download/confirmation.aspx?id=48145
[3]: http://www.lfd.uci.edu/~gohlke/pythonlibs/#opencv
[4]: http://docs.opencv.org/2.4/
[5]: http://docs.opencv.org/3.1.0/index.html
