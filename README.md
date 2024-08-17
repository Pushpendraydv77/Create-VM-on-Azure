# Lets create a VM (Virtual Machine)  Microsoft Azure 

NOTES:- Before starting you should have a Azure account with some credits in it or you can create a free one which give you $100 credit (am also using the free one account)

Once you Succesfully logined into the account you see a Bashboard like this once you see this click on   VIRTUAL MACHINE

![1ts](https://github.com/user-attachments/assets/98a10f6c-e993-4d67-ad30-9956e28d011b)

After that you see this page here you get the information about all Virtual Machines and click on CREATE  

![2](https://github.com/user-attachments/assets/b8e1b867-02f1-4175-8e81-53e822efcd2c)

Once you click created it will give to two options create a new virtual machine or create a virtual machine with preset configration  we will be going with first option 

![3](https://github.com/user-attachments/assets/dbd3ce8d-6343-492f-b7a6-0f7e7715cf65)

Once you have done above steps you greated with this page here you have to enter your basic information about your virtual machine. Like what Subscription you will be using with which Resource group,Enter the Virtual Machine Name it's Region etc. 

![4](https://github.com/user-attachments/assets/312b0dda-2dab-4e4a-9b08-8701327d4d2b)

After entring all required information hit next 

Once that done you can select which OS (operating system) you want (or image)
am going with Ubuntu Server LTS 24.. you can choose any once you have selected the os you have to choose VM Architecture you can go with Arm64 or X64 once choosen you can select the Size of the vm its depend on the load you will be putting on the server am going with Standard 1vcore cpu and 1gb ram 

NOTE: size of vm is also depends upone with what operating system you going with if you are going with Windows you might have to go with alteast 4gb ram and 2vcore cpu 

![5](https://github.com/user-attachments/assets/b8555412-0965-4c2d-8f90-0a6c4a7128de)

After selecting os,size now you have to select the authentication type you can go with a Password or SSH key (i will be going with SSH becoz it's more secure) we will be using this when we are going to connect to our vm 

First give a username to your vm, then select Generate new key pair (it will create a new ssh key pair if you already have a keypair you can use that) select SSH key type (am going with RSA format) once that done give a name to you SSH key pair (it can be any just keep in mind thta it is the only what to connect to your vm if you loose this key you may not able to access your VM)

![6](https://github.com/user-attachments/assets/765487b5-4385-4975-9e42-7acf4371b342)

Scrole down and you found inbound port setting port 22 is used by ssh so its already enabled you can select others too like i did.

![7 port open ](https://github.com/user-attachments/assets/f4480beb-ded4-4f96-a77d-d1dc63dc1c3f)

Now you can select how much storage you want in the system (same as os and size of vm its also depends on your work load)

![8 disk](https://github.com/user-attachments/assets/4685095f-7e10-48c5-b9aa-7ed143a0cafb)

After that hit Create (you can customize it even more but for our use case it is more then enough) it also show how much this vm running cost is mine it less but its depend the size of the vm if you go with more powerfull specs it will cost more  

![9 creat ](https://github.com/user-attachments/assets/dfe68baa-bd33-4af0-9eb0-f79094004ef5)

Once review process is done it will prompt you to download the SSH key just hit Download 

![10 downalodo ssh key](https://github.com/user-attachments/assets/4e723ead-63c6-4b5b-a805-9362146f062f)

If every thing os good you see this page here you can check status of you vm it's public ip to connect to it also you can start,stop or delete the vm and many more take few min. and explore then 

![11](https://github.com/user-attachments/assets/b0020754-7fdb-4500-9137-f194dc53b29d)

# Now lets connect to your VM form your remote PC 

TO do that open any terminal in the folder where you have stored your SSH(am using my WSL with Ubunut) and type 

``` ssh -i ssh-key-name username@public_ip ```

NOTE:- if its thow any error like WARNING: UNPROTECTED PRIVATE KEY FILE ! relex it's just a linux security feature you just have to chnage the files permission 

Run the command

``` chmod 400 your-ssh-key-name ```

After run the above command again 

``` ssh -i ssh-key-name username@public_ip ```

And you will able to access your VM 

![14 done](https://github.com/user-attachments/assets/8b383715-748c-4d42-bb57-db3b63378fba)








#this is how to create a vm and access it in Azure 



