# Who would care

nxRTOS is a RTOS implementation, serve as a low layer framework to firmware development on embedded platform. 
There is an Open Source version free available, for any firmware developer may interested.
From economic perspective, the consumer electrical maker with high volume massive production using micro-controller, may interested for BOM cost reduction. For example, a typical Cortex-M0 (with 10s KB RAM) cost less 1$ and Corte-M4 (with 100s KB RAM) cost 2 to 3$, if an Cortex-M0 can replace M4, it means 1 to 2$ cost saving on each single unit production. 
To all battery powered device, if the replacement can be done, it may bring double or triple service time between changing or charging battery. 

For example iRobot may interested. For each BLDC (Brushless DC Motor) there is a dedicate micro-controller, many use Cortex-M4 and few use Cortex-M0. By using nxRTOS it would be much more possible to use Cortex-M0 to replace Cortex-M4.
