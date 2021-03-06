/**
  @page USBD_CCID  USB Device Specification for Integrated Circuit(s) Cards Interface Devices example (CCID)
  
  @verbatim
  ******************** (C) COPYRIGHT 2014 STMicroelectronics *******************
  * @file    readme.txt 
  * @author  MCD Application Team
  * @version V1.0.0
  * @date    31-January-2014
  * @brief   Description of the USB Device CCID example
  ******************************************************************************
  *
  * Licensed under MCD-ST Liberty SW License Agreement V2, (the "License");
  * You may not use this file except in compliance with the License.
  * You may obtain a copy of the License at:
  *
  *        http://www.st.com/software_license_agreement_liberty_v2
  *
  * Unless required by applicable law or agreed to in writing, software 
  * distributed under the License is distributed on an "AS IS" BASIS, 
  * WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
  * See the License for the specific language governing permissions and
  * limitations under the License.
  *   
  ******************************************************************************
   @endverbatim

   
@par Example Description 

This example shows CCID class implementation. 

When plugged into host (WinXP, Windows7), The STM32 device appears as a
smart card reader device using the windows native CCID driver.

For WinXP users, a windows update may be needed in order to download the CCID driver
"usbccid.sys".

Please note that although the USB CCID class implements all the CCID commands, the smartcard
interface (in file smartcard.c) implements only the "Answer to Reset" 
following a reception of IccPowerOn command from host.


@par Hardware and Software environment 

   - This example runs on STM32F072xB devices
   - This example has been tested with STM32072B-EVAL and can be easily tailored
     to any other supported device and development board.

   - STM32072B-EVAL Set-up
       - Use CN4 connector to connect the board to a PC host through USB cable
       - Insert the Smart card in the CN19 connector.
	   - The device shall be recognized as the CCID smart card reader device, 
       It shall be verified from the Device Manager


@par How to use it ?

 + EWARM
    - Open the usbd_ccid.eww workspace.
    - In the workspace toolbar select the project config: 
    - Rebuild all files: Project->Rebuild all
    - Load project image: Project->Debug
    - Run program: Debug->Go(F5)

 + MDK-ARM
	- Open the usbd_ccid.uvproj project
	- Rebuild all files: Project->Rebuild all target files
    - Load project image: Debug->Start/Stop Debug Session
    - Run program: Debug->Run (F5)    
	
 + TrueSTUDO
    - Open the TrueSTUDIO toolchain.
    - Click on File->Switch Workspace->Other and browse to TrueSTUDIO workspace directory.
    - Click on File->Import, select General->'Existing Projects into Workspace' and then click "Next". 
    - Browse to the TrueSTUDIO workspace directory, select the project.
    - Rebuild all project files: Select the project in the "Project explorer" 
      window then click on Project->build project menu.
    - Run program: Run->Debug (F11)
    
 * <h3><center>&copy; COPYRIGHT STMicroelectronics</center></h3>
 */
