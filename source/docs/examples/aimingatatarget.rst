Aiming at a Target
==================

Knowledge and Equipment Needed
------------------------------

- Robot with a vision system running PhotonVision
- Target
- Ability to track a target by properly tuning a pipeline

Code
-------

Now that you have properly set up your vision system and have tuned a pipeline, you can now aim your robot/turret at the target using the data from PhotonVision. This data is reported over NetworkTables and includes: latency, whether there is a target detected or not, pitch, yaw, area, skew, and target pose relative to the robot. This data will be used/manipulated by our vendor dependency, PhotonLib. The documentation for the Network Tables API can be found :ref:`here <docs/programming/nt-api/nt-api:Getting Target Information>` and the documentation for PhotonLib :ref:`here <docs/programming/photonlib/adding-vendordep:What is PhotonLib?>`. For right now, all we will be using is yaw. In this example, while the operator holds a button down, the robot will turn towards the goal using the P term of a PID loop. To learn more about how PID loops work, how WPILib implements them, and more, visit  `Advanced Controls (PID) <https://docs.wpilib.org/en/stable/docs/software/advanced-control/introduction/index.html>`_ and `PID Control in WPILib <https://docs.wpilib.org/en/stable/docs/software/advanced-controls/controllers/pidcontroller.html#pid-control-in-wpilib>`_.

The following example is from the PhotonLib example repository (`Java <https://github.com/PhotonVision/photonvision/tree/master/photonlib-java-examples/src/main/java/org/photonlib/examples/aimattarget>`_/`C++ <https://github.com/PhotonVision/photonvision/tree/master/photonlib-cpp-examples/src/main/cpp/examples/aimattarget>`_).

.. tab-set::

    .. tab-item:: Java

       .. rli:: https://raw.githubusercontent.com/PhotonVision/photonvision/master/photonlib-java-examples/src/main/java/org/photonlib/examples/aimattarget/Robot.java
         :language: java
         :linenos:

    .. tab-item:: C++ (Header)

       .. rli:: https://raw.githubusercontent.com/PhotonVision/photonvision/master/photonlib-cpp-examples/src/main/cpp/examples/aimattarget/include/Robot.h
         :language: c++
         :linenos:

    .. tab-item:: C++ (Source)

       .. rli:: https://raw.githubusercontent.com/PhotonVision/photonvision/master/photonlib-cpp-examples/src/main/cpp/examples/aimattarget/cpp/Robot.cpp
         :language: c++
         :linenos:
