<p align="center">
<img src="https://i.imgur.com/hOUBSUI.png" height="80%" width="80%" alt="Microsoft Active Directory Logo"/>
</p>


<h2>Managing Accounts and Group Policy</h2>

<p>
</p>
<p>
In this lab we'll be dealing with account lockouts and password resets. As well as Enabling and Disabling Accounts. Then finally, we'll be Observing some Authentication and Security Logs.
</p>
<br />

<p>
While logged into the DC we'll first start by Configuring the Account Lockout Policy withing the GPO (Group Policy Object): Account lockout duration, Account lockout threshold, Reset account lockout counter. Then after, we'll apply the Policies and make sure to apply the GPO immediately by logging into Client-1, then open up 'Command Prompt'. In the Command Prompt type "gpupdate /force", If we don't dont apply GPO immediately then it'll take around 90 minutes for the Group Policy to refresh. 
</p>

<p>
<img src="https://i.imgur.com/6p6RRD9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<br />

<p>
Here we are logged into Client-1 to apply GPO immediately and as we can see it was successful updated. 
</p>

<p>
<img src="https://i.imgur.com/xfiiktj.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>  
</p>
<p>

<p>
Now we'll log out of Client-1 and attempt to enter wrong password in 6 times to lock ourselfs out and then observe it on the DC then unlock the account, reset password and attempt logging in. 
</p>
<br />

<p>
<img src="https://i.imgur.com/11GrNvV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p>
Now that we are locked out, we will then go back to DC and search up the user and unlock the account then click apply. 
</p>
<br />

<p>
<img src="https://i.imgur.com/QrrJjDL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p>
As you can see it was a success, we were able to login onto Client-1 with 'beti.taq' user (random user selected out of the 10,000 we have in the employee OU).
</p>
<br />

<p>
<img src="https://i.imgur.com/14Kk17j.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p>
Now we will log back off of Client-1 and go onto DC to disable user (beti.taq). We will first observe what happens when tried to log back on Client-1 with disable user account. Many reason why accounts would be enable/disable, but mainly for new hires/promotions or someone gets fired/demoted.
</p>
<br />

<p>
<img src="https://i.imgur.com/RbxS7of.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p>
We attempted to log back in with an disable account user and got this message.
</p>
<br />

<p>
<img src="https://i.imgur.com/BzWkkfH.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p>
Then once we enabled the account, we were able to sucessfully log back into Client-1 with user.
</p>
<br />

<p>
<img src="https://i.imgur.com/6QuQ66D.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p>
Now for us to Observe some Authentication and Security Logs, we will have to oberseve in on Client-1. But since we're logged into user beti.taq, we will have to run application 'eventvwr.msc' as administrator. So it will prompt us to log in as admin then we'll be able to Observe some Authentication and Security Logs.
</p>
<br />

<p>
<img src="https://i.imgur.com/UwLoMmT.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<p>
<img src="https://i.imgur.com/0WxIPqA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
