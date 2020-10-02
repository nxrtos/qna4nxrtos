# Is this software complete and ready to go-to-market? or still in development? What are the milestones and timelines?

There still are works to be done to official release, but major features are available, and couple of demo project are up running on several supported evaluation boards.  

The OpenSource version is available for public access, can be used to learn and practice the new concept introduced by nxRTOS. 

nxRTOS invents a new concept of RTOS_Job and through API of commit_Job to kernel to create new thread. The thread can be either a Long-Live-Thread (which is same as Task in conventional RTOS) or a Short-Live-Thread (which is unique from nxRTOS). 

As this moment API function commit_Job is functional to commit immediate Job and/or deferred Job (this can replace SoftTimer in conventional RTOS), as well as Mutex conditional Job, which competing to acquire Mutex before run the Job. It is still a question and discussion if do need a Semaphore conditional Job to implement.

It is expected to have a much cleaned code and API refactor by end of 2020. There also a lot documentation work to be done by the time.

As this moment only Cortex-M0/3/4 supported. Support other CPU architecture will to subject to customer demanding and development force available. 
