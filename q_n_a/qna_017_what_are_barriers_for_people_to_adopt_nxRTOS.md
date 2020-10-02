# what are barriers for people to adopt nxRTOS

First of all, the nxRTOS is an RTOS implementation. RTOS brings lot of benefits to firmware development, but there are some knowledge and concepts required to mastering RTOS. This applies to nxRTOS as well.

Second nxRTOS extend conventional RTOS to bring up new concepts, like Short-Live-Thread. It leads to a possible different programming model, (for example Active Object). So the training and tech support likely to be necessary. If the trainee have RTOS knowledge already, it should not to be difficult to understand nxRTOS and use it.

There is an OpenSource version of nxRTOS available for free of charge. The API is same to commercial version. The difference is the OpenSource version does not support preemption between Short-Live-Thread, rather than, when a higher priority of  Short-Live-Thread ready to run, the nxRTOS scheduler promote the priority of current Short-Live-Thread, expedite current Short-Live-Thread to complete and after then execute new  Short-Live-Thread. Through OpenSource version, people can learn the concept and practice on supported evaluation boards. Many of supported evaluation boards are low cost below $50. 
