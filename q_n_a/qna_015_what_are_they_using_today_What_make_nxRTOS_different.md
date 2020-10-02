# what are they using today? Why nxRTOS is different?

RTOS provides many benefits to firmware development on embedded system. There are ton of books and articles regarding RTOS. 
Check Wikipedia could find a lot related information.
With RTOS firmware development can construct on multi task model, and each task can run on designated priority, with preemption feature (which many RTOS support,) in place, the high priority of task always get execution than lower priority of task, so the real-time to be satisfied. 

While develop nxRTOS, there 3 RTOSes use as reference. FreeRTOS, NuttX, Zephyr Project. For technical reason, the task always programmed as a forever loop and (almost) never return. I name the task to Long-Live-Thread. For each task created, a chunk RAM has to be assigned as stack space for the task, as the task runs forever, the assigned stack space has to be exclusively belong to the task. When create multiple task, it means many of exclusive stack space taken.
nxRTOS supporta Short-Live-Thread, which means the Thread has to return, run to termination and release the stack space at the end. With unique Short-Live-Thread, the programming model could reach much more potential way and to be better to fit event handling model. Active Object is one of UML model, with nxRTOS it is much easier to construct firmware in AO (Active Object) model. 

We find it almost impossible to start second task when trying to deploy FreeRTOS on many Cortex-M0 based platform. With single task, the priority differential is meaningless and preemption is impossible, and so the real-time feature lost. With nxRTOS on Cortex-M0, multiple Short-Live-Thread can running in parallel, high priority thread can preempt lower priority thread, and so real-time feature is guaranteed.   
