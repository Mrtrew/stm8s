/** @page UART1_Polling Communication between UART1 and UART3 using flags


  @par Example description

  This example provides a basic communication between UART1 and UART3 using flags.
  First, the UART1 sends TxBuffer to UART3. The UART3 reads the received data and
  store it into RxBuffer.
  The received data is then compared with the send ones and the result of this 
  comparison is stored in the "TransferStatus" variable.   

  UART1 and UART3 configured as follow:
   - BaudRate = 230400 baud  
   - Word Length = 8 Bits
   - One Stop Bit
   - Even parity
   - Receive and transmit enabled
   - UART1 Clock disabled


  @par Directory contents

  - UART1\UART1_Polling\main.c                    Main file containing the "main" function
  - UART1\UART1_Polling\stm8s_conf.h              Library Configuration file
  - UART1\UART1_Polling\stm8s_it.c                Interrupt routines source (not used in this example)
  - UART1\UART1_Polling\stm8s_it.h                Interrupt routines declaration
  - UART1\UART1_Polling\stm8_interrupt_vector.c   Interrupt vectors table


  @par Hardware and Software environment

  - This example runs only on STM8S208 and STM8S207 devices.
  
  - This example has been tested with STMicroelectronics STM8/128-EVAL evaluation
    board (STM8S208) and ST Visual Develop (STVD) toolchain (Cosmic compiler).
    And can be easily tailored to any other supported device and development board.

  - STM8/128-EVAL Set-up
    - Connect UART1_Tx(PA.05) to UART3_Rx(PD.06) and UART1_Rx(PA.04) to UART3_Tx(PD.05)
      or connect a null-modem female/female RS232 cable between CN15 and CN13.


  @par How to use it ?

  In order to make the program work, you must do the following :
  - Create a project and setup all project configuration
  - Add the required Library files :
    - stm8s_clk.c
    - stm8s_exti.c
    - stm8s_uart1.c
    - stm8s_uart3.c
  - Edit stm8s.h file to select the device you are working on (#define STM8S208, in this case).
  
  @b Tip: You can tailor the provided project template to run this example, for more
          details please refer to "stm8s_fwlib_um.chm" user manual; select "Peripheral Examples"
          then follow the instructions provided in "How to proceed" section.   
  - Rebuild all files: Build-> Rebuild all. 
  - Load project image: Debug->Start Debugging
  - Run program: Debug->Run (Ctrl+F5)
    
  */

/******************* (C) COPYRIGHT 2009 STMicroelectronics *****END OF FILE****/
