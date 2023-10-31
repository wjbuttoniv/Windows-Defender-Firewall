# Configure Firewall Rules Using Windows Defender Firewall

### In this project, the objective is to get familiar with Windows Defender's Firewall rules, as well as configure an inbound and outbound rule

## Step 1: To Start, we need to open Windows Security

![[Pasted image 20231031111813.png]]![[Pasted image 20231031111835.png]]

### Next, we need to click on "Firewall and Network Protection"

![[Pasted image 20231031111924.png]]

### This page shows us the status of the firewall for each of the Following
- Domain Network
- Private Network
- Public Network
![[Pasted image 20231031112122.png]]

### For this example, we are going to start with the domain network

### Here, we can verify that the Defender firewall is set to "On"

![[Pasted image 20231031112349.png]]

### Note the above in blue, we won't be using this here but clicking this checkbox would block all incoming connections on this network, even ones that are normally allowed

### Now, we can check out the Private Network

![[Pasted image 20231031112547.png]]

### Note that we have the same option here to verify that the network firewall is enabled, as well as the option to block all incoming connections

### Now we check the Public Network Firewall, so let's go there

![[Pasted image 20231031112741.png]]

## Step 2: Allow an Application through the firewall

### Now that we have verified that all of the firewalls in defender are enabled, we can allow a specific application through. In this case, it will be firefox

### First, we need to click "Allow an app through firewall"

![[Pasted image 20231031113016.png]]

### This will bring up the allowed apps page in Defender's Firewall Section

![[Pasted image 20231031113059.png]]

### We are going to enable Firefox to communicate on the public network, as it is already enabled on the private network

### To do that, we want to make sure we click the checkbox that says "Public" and not "Private"

![[Pasted image 20231031113303.png]]

## Step 3: Firewall Advanced Security

### Now we are going to take a look at some of the advanced security features of Defender's Firewall

### For this example, we are going to:
#### Allow the connection for Key Management Service on the Domain and Private Network
#### Deny the connection for Key Management Service on the Public Network

### First, we need to click on "Advanced Settings"

![[Pasted image 20231031113629.png]]

### This displays the Advanced Security Window

![[Pasted image 20231031113749.png]]

### There's quite a lot of content on this page, but for the sake of this example, we are going to click on "inbound rules"

![[Pasted image 20231031114514.png]]

### This displays a page with a list of the inbound rules for the firewall

![[Pasted image 20231031114902.png]]

### Note the current status of the Key Management Service

![[Pasted image 20231031115035.png]]

### By right-clicking and selecting properties, the general rule for the service is shown

![[Pasted image 20231031115311.png]]

### In the Advanced Section, the profiles that rules apply to are shown

![[Pasted image 20231031115547.png]]

### Public should not be enabled, so we will disable it

![[Pasted image 20231031115648.png]]

### As the objective is to block traffic on the public network, there needs to be an inbound rule created that is consistent with that objective. For that purpose, we need to copy the rule

![[Pasted image 20231031120308.png]]

### In the General Tab, we change "allow the connection" to "block the connection"

![[Pasted image 20231031120354.png]]

### In the Advanced tab, we change the profiles to just "Public"

![[Pasted image 20231031120450.png]]

### The overview panel now shows the correct rules

![[Pasted image 20231031120734.png]]

