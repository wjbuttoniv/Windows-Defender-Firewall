# Configuring Firewall Rules Using Windows Defender Firewall

In this project, the goal is to become acquainted with Windows Defender Firewall rules and their configuration, including both inbound and outbound rules.

## Step 1: Accessing Windows Security

To begin, let's initiate the process by accessing Windows Security. 

![a](https://github.com/wjbuttoniv/Windows-Defender-Firewall/blob/main/Windows-Defender-Firewall/Pasted%20image%2020231031111813.png?raw=true)
![b](https://github.com/wjbuttoniv/Windows-Defender-Firewall/blob/main/Windows-Defender-Firewall/Pasted%20image%2020231031111835.png?raw=true)

Subsequently, navigate to the "Firewall and Network Protection" section.

![c](https://github.com/wjbuttoniv/Windows-Defender-Firewall/blob/main/Windows-Defender-Firewall/Pasted%20image%2020231031111924.png?raw=true)

This page provides an overview of the firewall status for the following network types:
- Domain Network
- Private Network
- Public Network

![d](https://github.com/wjbuttoniv/Windows-Defender-Firewall/blob/main/Windows-Defender-Firewall/Pasted%20image%2020231031112122.png?raw=true)

For the purpose of this example, we will start by focusing on the domain network.

Here, you can confirm that Windows Defender Firewall is enabled.

![e](https://github.com/wjbuttoniv/Windows-Defender-Firewall/blob/main/Windows-Defender-Firewall/Pasted%20image%2020231031112349.png?raw=true)

Please note the option in blue. Although we won't be utilizing it here, selecting this checkbox would block all incoming connections on this network, including those typically allowed.

Now, let's proceed to inspect the Private Network.

![f](https://github.com/wjbuttoniv/Windows-Defender-Firewall/blob/main/Windows-Defender-Firewall/Pasted%20image%2020231031112547.png?raw=true)

Similarly, in this section, you can verify whether the network firewall is enabled and choose to block incoming connections if desired.

Now, let's explore the Public Network Firewall settings.

![g](https://github.com/wjbuttoniv/Windows-Defender-Firewall/blob/main/Windows-Defender-Firewall/Pasted%20image%2020231031112741.png?raw=true)

## Step 2: Allowing an Application through the Firewall

After ensuring that Windows Defender Firewall is enabled for all network types, we can proceed to allow a specific application through. In this case, we will use Firefox as an example.

Initiate this process by selecting "Allow an app through firewall."

![h](https://github.com/wjbuttoniv/Windows-Defender-Firewall/blob/main/Windows-Defender-Firewall/Pasted%20image%2020231031113016.png?raw=true)

This action will bring up the allowed apps page within Windows Defender Firewall.

![i](https://github.com/wjbuttoniv/Windows-Defender-Firewall/blob/main/Windows-Defender-Firewall/Pasted%20image%2020231031113059.png?raw=true)

We intend to enable Firefox for communication on the public network, provided it is already enabled on the private network.

To achieve this, ensure that you select the checkbox marked "Public" rather than "Private."

![j](https://github.com/wjbuttoniv/Windows-Defender-Firewall/blob/main/Windows-Defender-Firewall/Pasted%20image%2020231031113303.png?raw=true)

## Step 3: Exploring Firewall Advanced Security

Now, let's delve into some of the advanced security features offered by Windows Defender Firewall. In this example, we will:

- Allow the connection for Key Management Service on the Domain and Private Network.
- Deny the connection for Key Management Service on the Public Network.

Commence by clicking on "Advanced Settings."

![k](https://github.com/wjbuttoniv/Windows-Defender-Firewall/blob/main/Windows-Defender-Firewall/Pasted%20image%2020231031113629.png?raw=true)

This action will display the Advanced Security Window.

![l](https://github.com/wjbuttoniv/Windows-Defender-Firewall/blob/main/Windows-Defender-Firewall/Pasted%20image%2020231031113749.png?raw=true)

While there is a wealth of information on this page, for the sake of this example, we will navigate to the "inbound rules."

![m](https://github.com/wjbuttoniv/Windows-Defender-Firewall/blob/main/Windows-Defender-Firewall/Pasted%20image%2020231031114514.png?raw=true)

This will present a list of inbound rules for the firewall.

![n](https://github.com/wjbuttoniv/Windows-Defender-Firewall/blob/main/Windows-Defender-Firewall/Pasted%20image%2020231031114902.png?raw=true)

Take note of the current status of the Key Management Service.

![o](https://github.com/wjbuttoniv/Windows-Defender-Firewall/blob/main/Windows-Defender-Firewall/Pasted%20image%2020231031115035.png?raw=true)

By right-clicking and selecting "properties," you can view the general rule for the service.

![p](https://github.com/wjbuttoniv/Windows-Defender-Firewall/blob/main/Windows-Defender-Firewall/Pasted%20image%2020231031115311.png?raw=true)

In the Advanced Section, the profiles to which the rules apply are displayed.

![q](https://github.com/wjbuttoniv/Windows-Defender-Firewall/blob/main/Windows-Defender-Firewall/Pasted%20image%2020231031115547.png?raw=true)

Since the Public profile should not be enabled, we will disable it.

![r](https://github.com/wjbuttoniv/Windows-Defender-Firewall/blob/main/Windows-Defender-Firewall/Pasted%20image%2020231031115648.png?raw=true)

As the objective is to block traffic on the public network, an inbound rule consistent with this goal needs to be created. To accomplish this, we will copy the rule.

![s](https://github.com/wjbuttoniv/Windows-Defender-Firewall/blob/main/Windows-Defender-Firewall/Pasted%20image%2020231031120308.png?raw=true)

In the General Tab, we will modify "allow the connection" to "block the connection."

![t](https://github.com/wjbuttoniv/Windows-Defender-Firewall/blob/main/Windows-Defender-Firewall/Pasted%20image%2020231031120354.png?raw=true)

In the Advanced tab, we will adjust the profiles to include only "Public."

![u](https://github.com/wjbuttoniv/Windows-Defender-Firewall/blob/main/Windows-Defender-Firewall/Pasted%20image%202023103

1120450.png?raw=true)

The overview panel will now display the appropriate rules.

![v](https://github.com/wjbuttoniv/Windows-Defender-Firewall/blob/main/Windows-Defender-Firewall/Pasted%20image%2020231031120734.png?raw=true)

In conclusion, this project has provided a comprehensive overview of Windows Defender Firewall rules and their configuration. We began by accessing Windows Security and checking the firewall status for different network types. Then, we explored how to allow specific applications through the firewall, using Firefox as an example. Finally, we delved into the advanced security features of Windows Defender Firewall, demonstrating how to customize inbound rules to control network traffic effectively. By following these steps, users can enhance the security and functionality of their Windows operating systems while managing network access with precision.
