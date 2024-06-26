# Fren Suipport

![image](https://github.com/do0x0ob/suiHackathon/assets/153002627/6a45a102-45a0-4168-968f-2d9f73e942c6)

**Fren Suipport** is a platform themed around the **Suifrens** NFT universe.<br/>

The primary function of this platform is to facilitate the exchange of labor and assets in the web3 world, offering a variety of features including public tasks, private tasks, charity crowdfunding, and product crowdfunding.<br/>
This project also a learning task module that uses on-chain records to retain all data, ensuring fair distribution of rewards.<br/>
<br/>
Currently, the first phase has implemented the public tasks feature.<br/>
<br/>
Fren Suipport aims to enable individuals without any web3 assets to seamlessly enter the web3 world. Without relying on centralized exchanges, users can earn their first web3 assets directly through activities such as learning, providing labor, and participating in submission competitions.

***For more details about our project, just head to our homepage and scroll down.***
<br>

![image](https://github.com/u2789011/suiHackthon/assets/153002627/e1b07300-09ba-49db-8b51-5c8a2466b2be)


<br/>

**Links:** 
- Web: <https://frensuipport.vercel.app/>
- Does: <https://aa5961311s-organization.gitbook.io/fren-suipport>
- Git Repo: <https://github.com/u2789011/suiHackthon>

*Powered by Fren Suipport team*
<br/>
<br/>
<br/>

---
## Public Tasks User Guide (Currently on Sui Testnet)

### 0. Overview
#### This is the homepage for public tasks. Our public task model is designed with the following features:
- ***Striving for Transparency and Openness:*** Anyone can submit their work without needing permission. Certified works will be frozen and preserved on the chain using Sui's Freeze Object function.
- ***On-chain Contract with Direct Bonus Distribution:*** Participants can confirm the existence of the prize before starting the task. The automatic reward distribution mechanism via smart contracts ensures the accuracy of the distributed amount.

#### The homepage has 3 tabs:
- ***All Tasks:*** Displays all currently published tasks. Tasks can be accepted from the task card's bottom section.
- ***On Going Tasks:*** Displays tasks that have been accepted. The task cards have a "Submit Task" button at the bottom, providing the ability to update task information and submit.
- ***Published by Me:*** Displays tasks published by you or tasks where you have been assigned as the task MOD, providing access to manage tasks (for creators) and task list management (for task MODs).

![image](https://github.com/do0x0ob/suiHackathon/assets/153002627/b8a09a13-fc51-4bd8-b3b7-aca700ff23b2)

#### The Foldable Sidebar :
- ***My Suifren:*** Displays the Suifren associated with the current wallet address.
- ***Port Temple Relics:*** "Relics" refer to a series of Suifren accessory NFTs that users can add to their Suifrens to utilize specific functions.
  - User can publish tasks while the Suifren NFT is equipped with a "trident" item. 
  - Currently, we use the existing Suifren accessory item "Magic Wand" to represent the "Trident" to demonstrate its functionality in Fren support. It will be replaced once the 
  new contracts are ready.
- ***PASUIPORT:*** This feature is still under construction. It will use the exclusive "Transfer to Object" concept in Sui to display the user's achievements, and users can decide which achievements they want to showcase.

![image](https://github.com/do0x0ob/suiHackathon/assets/153002627/930f754c-b22a-4a18-af62-7711246fac68)

### 1. Publish Task
  - The creator needs to have a Suifren NFT equipped with a "Trident" item to publish tasks.
  - The creator needs to deposit a Coin object on the Sui chain as the funding source and set the reward amount for each piece.
  - The creator can assign a task MOD responsible for the subsequent certification of task submissions when publishing
    (currently, only one manager can be set, and you can designate yourself)
    
  ![image](https://github.com/u2789011/suiHackthon/assets/153002627/814ed343-02d1-41d1-a7e8-ff7e72678d0e)

#### Field Input Guide (We will optimize the filling method in the future; for now, please fill in manually)

| Field                          | Description                                                            | Example                                                             |
|--------------------------------|------------------------------------------------------------------------|---------------------------------------------------------------------|
| **Reward Type**                | The currency type of the reward pool                                   | `0x2::sui::SUI`                                                     |
| **Task Name**                  | The name of your task                                                  | `Develop a Web3 dApp`                                               |
| **Description**                | Task description text                                                  | `Detailed description of the task`                                  |
| **Task Image URL**             | Task image                                                             | `https://example.com/image.png`                                     |
| **Task Area**                  | The applicable area for the task                                       | `WorldWide`                                                         |
| **Task MOD**                   | The Sui address of the designated task manager                         | `0x3cf1567de31e74baa94b0ab48b3ce57535e3799dac7e0d1da2c7a9058e50a9d4`|
| **Task Fund**                  | The ObjectID of the reward                                             | `0x18d942f98915a729f751df90351175311d5918f962ebc18db43eac0f0c245`   |
| **Reward Amount**              | The reward amount for each approved submission                         | `100`                                                               |
| **Proof of Completion Image URL** | The image link for the completion proof NFT                         | `https://example.com/proof.png`                                     |

### 2. Accept Task
- When users see a task they want to execute, they can click Accept Task under the All Task tab to mint a Task Sheet associated with the main task.
- In the future, this Task Sheet will be used as a record of the task results.
<br>

![image](https://github.com/u2789011/suiHackthon/assets/153002627/1a62147b-971c-4cee-b8c1-f7cb2ebc4517)


### 3. Submit Task Sheet
- When users need to edit a task record, they can click the Submit Task Sheet button to enter the task sheet editing window. After entering the required information, they need to click Update first. This will modify the task sheet fields on the blockchain.
- When users need to submit the task sheet to the MOD, they can click Submit. The task will be marked as Pending Review and transferred to the MOD.
<br>

![image](https://github.com/u2789011/suiHackthon/assets/153002627/598f3c68-71ec-470b-bcb2-bf8bdfdfa55b)

### 4. MOD Reviews Task Sheet
- Once the task sheet is submitted, it will be transferred to the MOD's address. The MOD can find the entrance to review the task sheet under the Published by me tab by clicking View Submitted Tasks.
- In the window, the MOD can see all the task sheets related to the task, provide comments, and approve them (currently, the task sheet content can only be viewed on the blockchain explorer).
- If the MOD chooses not to approve the task sheet, it will be returned to the executor's wallet, where the user can complete the task and resubmit it.
<br>

![image](https://github.com/u2789011/suiHackthon/assets/153002627/d0b1fe03-2b0f-420a-b40d-9e6fb41e5376)

### 5. Task Executor Receives Reward [The multi-selection feature is still under development]
- When the task sheet is approved by the MOD, the smart contract will automatically distribute the agreed-upon reward amount from the reward pool to the task executor.
- The TaskSheet will be permanently frozen on the blockchain using the freeze object function to preserve the record.
- At this point, a POC (Proof of Completion) will be minted and transferred to the task completer, thus concluding the public task process.
<br/>

*As you can see on the screenshot below, This transaction automatically disburses the reward, freezes the task sheet, and mints a Proof of Completion.*
<br>

![image](https://github.com/do0x0ob/suiHackathon/assets/153002627/8686c0a6-7fb3-4be7-bde8-901d1e817553)


---

## Main Sui Object
> Testnet Package: `0xc8e76738b2a255fe5a093a39f1eaa3b3ab869efcd62e4705c8790ceb7a532f02`

**0. Task Manager**
The object is created by invoking the init function when the contract is deployed, and it acts as a container to record the IDs of all tasks.

**1. Main Task**
Defines task fields, task manager, etc. Only those with the publication permission object can modify the task description.
It locks a Fund, which can be any Coin, specified when creating the task.

**2. Task Sheet**
Minted by users when they accept tasks on the front end. Only users with modification rights can change the content.
After completing the task, the record to be submitted is written on the task sheet. Once edited, it can be submitted.
The task sheet will be automatically transferred to the task manager (address specified by the task publisher) by the smart contract.

**3. POC(Proof of Completion)**
This object is minted and transferred to the completer's address when the task is approved. The image is specified by the task publisher.

---

## About the Team
**Fren Suipport**
> The team consists of 5 members from the ***Blockchain Research Club at National Chung Hsing University***.
> One of the members joined the club the day after meeting the others at the Sui Hacker House event in Taipei.
<br>

![image](https://github.com/u2789011/suiHackthon/assets/153002627/43e88b8f-58f7-4f9d-8467-ddca024a4a86)


---

## Project - TODOS
### 0. General Functions
- ~~Integrate SuiFren NFT Display~~ (Done By d0x0b, 20240615)
- Publish a Suifrens relics accessories collection
- ~~to grant different privileges and roles within the Fren Suipport world~~ (FrontEnd Done By d0x0b, 20240629)

### 1. Public Task Module
**Bugs**
- ~~Fix Approve Tasksheets Fuctions~~ (Done By d0x0b, 20240602)
- ~~Fix Reject Tasksheets Fuctions~~ (Done By d0x0b, 20240604)
- ~~Fix Submit Task Function~~ (Done By d0x0b, 20240531)
- ~~Fix Edit Description Function~~ (Done By d0x0b, 20240531)
- ~~Fix multi-selection Tasks on Tasksheets Review Panel~~ (Done By Ashley, 20240616)

**Features**
- Add a switch for task status.
- Add sponsored Gas for first timers to mint TaskSheets FREE.

### 2. Fundraising Module

### 3. Personal Task Module

### 4. Vendors Module
