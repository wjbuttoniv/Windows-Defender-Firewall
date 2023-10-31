# Configure Firewall Rules Using Windows Defender Firewall

### In this project, the objective is to get familiar with Windows Defender's Firewall rules, as well as configure an inbound and outbound rule

## Step 1: To Start, we need to open Windows Security

![a](https://github.com/wjbuttoniv/Windows-Defender-Firewall/blob/main/Windows-Defender-Firewall/Pasted%20image%2020231031111813.png?raw=true)
![b](https://github.com/wjbuttoniv/Windows-Defender-Firewall/blob/main/Windows-Defender-Firewall/Pasted%20image%2020231031111835.png?raw=true)

### Next, we need to click on "Firewall and Network Protection"

![c](https://github.com/wjbuttoniv/Windows-Defender-Firewall/blob/main/Windows-Defender-Firewall/Pasted%20image%2020231031111924.png?raw=true)

### This page shows us the status of the firewall for each of the Following
- Domain Network
- Private Network
- Public Network
![d](https://github.com/wjbuttoniv/Windows-Defender-Firewall/blob/main/Windows-Defender-Firewall/Pasted%20image%2020231031112122.png?raw=true)

### For this example, we are going to start with the domain network

### Here, we can verify that the Defender firewall is set to "On"

![e](https://github.com/wjbuttoniv/Windows-Defender-Firewall/blob/main/Windows-Defender-Firewall/Pasted%20image%2020231031112349.png?raw=true)

### Note the above in blue, we won't be using this here but clicking this checkbox would block all incoming connections on this network, even ones that are normally allowed

### Now, we can check out the Private Network

![f](https://github.com/wjbuttoniv/Windows-Defender-Firewall/blob/main/Windows-Defender-Firewall/Pasted%20image%2020231031112547.png?raw=true)

### Note that we have the same option here to verify that the network firewall is enabled, as well as the option to block all incoming connections

### Now we check the Public Network Firewall, so let's go there

![g](https://github.com/wjbuttoniv/Windows-Defender-Firewall/blob/main/Windows-Defender-Firewall/Pasted%20image%2020231031112741.png?raw=true)

## Step 2: Allow an Application through the firewall

### Now that we have verified that all of the firewalls in defender are enabled, we can allow a specific application through. In this case, it will be firefox

### First, we need to click "Allow an app through firewall"

![h](https://github.com/wjbuttoniv/Windows-Defender-Firewall/blob/main/Windows-Defender-Firewall/Pasted%20image%2020231031113016.png?raw=true)

### This will bring up the allowed apps page in Defender's Firewall Section

![i](https://github.com/wjbuttoniv/Windows-Defender-Firewall/blob/main/Windows-Defender-Firewall/Pasted%20image%2020231031113059.png?raw=true)

### We are going to enable Firefox to communicate on the public network, as it is already enabled on the private network

### To do that, we want to make sure we click the checkbox that says "Public" and not "Private"

![j](https://github.com/wjbuttoniv/Windows-Defender-Firewall/blob/main/Windows-Defender-Firewall/Pasted%20image%2020231031113303.png?raw=true)

## Step 3: Firewall Advanced Security

### Now we are going to take a look at some of the advanced security features of Defender's Firewall

### For this example, we are going to:
#### Allow the connection for Key Management Service on the Domain and Private Network
#### Deny the connection for Key Management Service on the Public Network

### First, we need to click on "Advanced Settings"

![k](https://github.com/wjbuttoniv/Windows-Defender-Firewall/blob/main/Windows-Defender-Firewall/Pasted%20image%2020231031113629.png?raw=true)

### This displays the Advanced Security Window

![l](https://github.com/wjbuttoniv/Windows-Defender-Firewall/blob/main/Windows-Defender-Firewall/Pasted%20image%2020231031113749.png?raw=true)

### There's quite a lot of content on this page, but for the sake of this example, we are going to click on "inbound rules"

![m](https://github.com/wjbuttoniv/Windows-Defender-Firewall/blob/main/Windows-Defender-Firewall/Pasted%20image%2020231031114514.png?raw=true)

### This displays a page with a list of the inbound rules for the firewall

![n](https://github.com/wjbuttoniv/Windows-Defender-Firewall/blob/main/Windows-Defender-Firewall/Pasted%20image%2020231031114902.png?raw=true)

### Note the current status of the Key Management Service

![o](https://github.com/wjbuttoniv/Windows-Defender-Firewall/blob/main/Windows-Defender-Firewall/Pasted%20image%2020231031115035.png?raw=true)

### By right-clicking and selecting properties, the general rule for the service is shown

![p](https://github.com/wjbuttoniv/Windows-Defender-Firewall/blob/main/Windows-Defender-Firewall/Pasted%20image%2020231031115311.png?raw=true)

### In the Advanced Section, the profiles that rules apply to are shown

![q](https://github.com/wjbuttoniv/Windows-Defender-Firewall/blob/main/Windows-Defender-Firewall/Pasted%20image%2020231031115547.png?raw=true)

### Public should not be enabled, so we will disable it

![r](https://github.com/wjbuttoniv/Windows-Defender-Firewall/blob/main/Windows-Defender-Firewall/Pasted%20image%2020231031115648.png?raw=true)

### As the objective is to block traffic on the public network, there needs to be an inbound rule created that is consistent with that objective. For that purpose, we need to copy the rule

![s](https://github.com/wjbuttoniv/Windows-Defender-Firewall/blob/main/Windows-Defender-Firewall/Pasted%20image%2020231031120308.png?raw=true)

### In the General Tab, we change "allow the connection" to "block the connection"

![t](https://github.com/wjbuttoniv/Windows-Defender-Firewall/blob/main/Windows-Defender-Firewall/Pasted%20image%2020231031120354.png?raw=true)

### In the Advanced tab, we change the profiles to just "Public"

![u](https://github.com/wjbuttoniv/Windows-Defender-Firewall/blob/main/Windows-Defender-Firewall/Pasted%20image%2020231031120450.png?raw=true)

### The overview panel now shows the correct rules

![v](https://github.com/wjbuttoniv/Windows-Defender-Firewall/blob/main/Windows-Defender-Firewall/Pasted%20image%2020231031120734.png?raw=true)
