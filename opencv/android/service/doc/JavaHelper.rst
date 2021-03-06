******************
Java OpenCV Loader
******************

.. highlight:: java
.. Class:: OpenCVLoader

Helper class provides common initialization methods for OpenCV library.

boolean initDebug()
-------------------

.. method:: static boolean initDebug()

    Loads and initializes OpenCV library from within current application package. Roughly it is analog of ``system.loadLibrary("opencv_java")``.

    :rtype: boolean;
    :return: returns true if initialization of OpenCV was successful.

.. note:: This method is deprecated for production code. It is designed for experimantal and local development purposes only. If you want to publish your app use approach with async initialization.

boolean initAsync()
-------------------

.. method:: static boolean initAsync(String Version, Context AppContext, LoaderCallbackInterface Callback)

    Loads and initializes OpenCV library using OpenCV Manager service.

    :param Version: OpenCV Library version.
    :param AppContext: application context for connecting to the service.
    :param Callback: object, that implements LoaderCallbackInterface for handling connection status (see BaseLoaderCallback).

    :rtype: boolean;
    :return: returns true if initialization of OpenCV starts successfully.

OpenCV version constants
-------------------------

.. data:: OPENCV_VERSION_2_4_2

    OpenCV Library version 2.4.2

Other constatnts
----------------

.. data:: OPEN_CV_SERVICE_URL

    Url for OpenCV Manager on Google Play (Android Market)