<h1 align="center">Secure Cloud Configuration - Part 1</h1>

<br>

<h2 align="center">Regulatory Compliance: Enable NIST 800-53</h2>

<p align="center">
<img width="700" src="https://github.com/user-attachments/assets/ba44e0c3-5ee1-4d97-b92a-13e15c4c6c1e" alt="Banner"/>

<br>

<br>

In the previous labs we performed some **Incident Response**, and we even **Remediated some Vulnerabilities** like Hardening the NSGs.

We also Captured our **Environment's Traffic** in an Insecured State for 24 hours & Recorded our **Security Metrics**.

<br>

In this lab, and in the subsequent ones, we’ll work towards **Securing our Environment**.

<br>

Basically in this lab we’re going to:

  -	Look at Microsoft Defender for Cloud’s **Secure Score**.
    
  -	Look at Microsoft Defender for Cloud’s **Recommendations**, and learn what that is.
    
  -	Enable MDC’s **Regulatory Compliance for NIST 800-53**.

<br>

>   <details close> 
>   
> **<summary> 💡 Note</summary>**
> 
> If you remember ➜ NIST 800-53 is the Security and Privacy control family.
> 
> It’s basically just a really large catalog of controls that you can use to either evaluate or help secure your environment.
> 
> And basically, when we enable the NIST 800-53 Regulatory Compliance in Azure – it’s going to show us things that we can do in Azure to secure our Environment that kind of align with NIST 800-53 controls.
> 
> And I think it’s really good, because it gives us a better intuition of what NIST 800-53 is for, and like how it’s used and why it’s useful.
>   
>   </details>

<br>

<br>

<details close> 
<summary> <h2>1️⃣ Inspect MDC Secure Score & Recommendations</h2> </summary>
<br>

The first thing we’re going to do is Inspect the [**Microsoft Defender for Cloud Secure Score**](https://learn.microsoft.com/en-us/defender-xdr/microsoft-secure-score?view=o365-worldwide)

We’ll go to the **Azure Portal** ➜ open **Microsoft Defender for Cloud**:

<br>

![azure portal](https://github.com/user-attachments/assets/9c1cce53-082a-4c9e-b6d5-7da25a14a9d7)

<br>

>   <details close> 
>   
> **<summary> 💡 </summary>**
> 
> Defender for Cloud provides us with a 🛡️ **Secure Score**.
> 
> It’s sort of a single metric that we can use to gage our Security Posture and how good it is.
>   
>   </details>

<br>

Then we can click on the **Recommendations** blade on the left side:

<br>

![azure portal](https://github.com/user-attachments/assets/9c1cce53-082a-4c9e-b6d5-7da25a14a9d7)

<br>

The interface will show us all the things that are contributing to our Environment’s **Security Score**.

<br>

  <details close> 
  
**<summary> 💡 </summary>**

It’ll show us areas that essentially have gaps:

➡️ So we can implement things in Azure & perform some Configurations in order to make our Security Score go Up.

  </details>

<br>

![azure portal](https://github.com/user-attachments/assets/9c1cce53-082a-4c9e-b6d5-7da25a14a9d7)

<br>

🔍 We can look through all the different **Recommendations** and get a good sense of what we can do to **Harden our Environment**.

<br>

  </details>

<h2></h2>

<details close> 
<summary> <h2>2️⃣ Enable NIST 800-53</h2> </summary>
<br>

The next thing we’re going to do is **Enable Regulatory Compliance for NIST 800-53**.

Basically this is kind of going to do the same thing as the **MDC Secure Score Recommendations** ➜ but it’ll do it in the “lens” of **NIST 800-53**.

<br>

  <details close> 
  
**<summary> 📝 Refresher</summary>**

<br>

[NIST 800-53](https://csrc.nist.gov/projects/cprt/catalog#/cprt/framework/version/SP_800_53_5_1_0/home) is a really large control catalog with a lot of different control families like:

-	 Access Control
-	 Identification and Authentication
-	 Incidence Response, etc.

<br>

![azure portal](https://github.com/user-attachments/assets/9c1cce53-082a-4c9e-b6d5-7da25a14a9d7)

<br>

These are all different categories ➜ and then inside of these there’s a lot of **Sub-Controls** essentially

For example: inside of **"SC - SYSTEM AND COMMUNICATION PROTECTION"** ➜ there's a lot of different Categories:

<br>

![azure portal](https://github.com/user-attachments/assets/9c1cce53-082a-4c9e-b6d5-7da25a14a9d7)

<br>

So when we enable NIST 800-53 Regulatory Compliance inside of Defender for Cloud ➜ it’s basically going to look at all the different Controls inside of NIST 800-53 and talk about different things we can do in our Environment that align with, for example, SC-7 or SC11:

<br>

![azure portal](https://github.com/user-attachments/assets/9c1cce53-082a-4c9e-b6d5-7da25a14a9d7)

<br>

Essentially it will suggest different implementations we can do in Azure to bring our Environment "Up to Par" with NIST 800-53.

In a way, show us Gaps in relation to Controls that exist in NIST 800-53.

  </details>

<br>








<br>

<br>

<br>

<br>











Adding [**NIST 800-53: Security and Privacy Controls for Information Systems and Organizations**](https://csrc.nist.gov/pubs/sp/800/53/r5/upd1/final) to **Microsoft Defender for Cloud**.

💡 [**Full Publication**](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-53r5.pdf).

To add NIST 800-53:

  - First inside the MDC home page ➜ click on the **Regulatory Compliance** blade on the left side:

<br>

![azure portal](https://github.com/user-attachments/assets/9c1cce53-082a-4c9e-b6d5-7da25a14a9d7)

<br>

  - Then at the top ➜ click on **Manage compliance policies**:

<br>

![azure portal](https://github.com/user-attachments/assets/9c1cce53-082a-4c9e-b6d5-7da25a14a9d7)

<br>

  - We'll then click on our **Subscription**:

<br>

![azure portal](https://github.com/user-attachments/assets/9c1cce53-082a-4c9e-b6d5-7da25a14a9d7)

<br>

  - Inside the **Security policy** blade ➜ under **Industry & regulatory standards**  ➜ click on the **"Add more standards"** button:

<br>

![azure portal](https://github.com/user-attachments/assets/9c1cce53-082a-4c9e-b6d5-7da25a14a9d7)

<br>

  - Add ```NIST 800-53 R5``` as a **Regulatory Compliance Standard**:

<br>

![azure portal](https://github.com/user-attachments/assets/9c1cce53-082a-4c9e-b6d5-7da25a14a9d7)

<br>


After waiting a while ➜ we can confirm that **NIST 800-53 R5** was successfully assigned to our Subscription ✅

<br>

![azure portal](https://github.com/user-attachments/assets/9c1cce53-082a-4c9e-b6d5-7da25a14a9d7)

<br>


⚠️ Again ➜ it takes some time for the policy to be added to our Environment ➜ but eventually it should appear inside of our MDC Dashboard ➜ under **Regulatory Compliance**:

<br>

![azure portal](https://github.com/user-attachments/assets/9c1cce53-082a-4c9e-b6d5-7da25a14a9d7)

<br>


>   <details close> 
>   
> **<summary> 📝 Explanation</summary>**
> 
> GO TO MIN 11 AND WRITE WHAT JOSH IS SAYING EXPLAINING NIST 800 53 !!!!!!!!!!!!
> 
> In our case we configured a bunch of Alerts ➜ and the fact that an **Incident was Created** ➜ is the beggining of our **Detection Phase**.
> 
>   </details>



<br>

<br>

<br>

<br>







> <details close> 
>   
> **<summary> 💡 </summary>**
> 
> This Incident gets triggered when Sentinel detects a Successful Login after Multiple Failed Attempts.
> 
> It indicates that a Brute Force Attack was Successfully Conducted.
> 
>   </details>

<br>

## Incident Description

<br>

➡️ This Incident involves observation of potential **Brute Force Attempts against a Windows VM**.

<br>

![azure portal](https://github.com/user-attachments/assets/9c1cce53-082a-4c9e-b6d5-7da25a14a9d7)

<br>

<br>

## Initial Response Actions

<br>

✔ Verify the Authenticity of the Alert or Report.

✔ Immediately Isolate the Machine and Change the Password of the affected User.

✔ Identify the Origin of the Attacks and determine if they are attacking or involved with anything else.

✔ Determine How and When the attack occurred.

✔ Are the NSGs not being locked down? If so ➜ check other NSGs.

✔ Assess the Potential Impact of the Incident.

✔ What Type of Account was it? What Permissions did it have?

<br>

<br>

## Detection & Analysis

<details close> 
<summary> <h3>🎯 Step-by-Step</h3> </summary>

<br>
  
**1️⃣** Set the **Severity**, the **Status** & the **Owner** of the Incident:

<br>

![azure portal](https://github.com/user-attachments/assets/014f7990-1462-435d-814c-b637a0cc8fe1)

<br>

<h2></h2>

<br>

**2️⃣** **View Full Details**

<br>

![azure portal](https://github.com/user-attachments/assets/85192897-8e6b-4373-9056-1119fd9bde61)

<br>

<h2></h2>

<br>

**3️⃣** Observe the **Activity Log**

<br>

**```Nothing to show here.```**

<br>

<h2></h2>

<br>

**4️⃣** Observe the **Entities** & **Incident Timeline**

<br>

![azure portal](https://github.com/user-attachments/assets/f3c2a5d6-044c-469d-b70a-c066fe2a29e3)

<br>

<h2></h2>

<br>

**5️⃣** **Investigate the Incident** and continue trying to **Determine the Scope**

<br>

![azure portal](https://github.com/user-attachments/assets/80a9eedd-d292-448f-b591-33c19b0a5936)

<br>

![azure portal](https://github.com/user-attachments/assets/7a073b8d-b577-43b8-885f-7cb587d152e1)

<br>

<h2></h2>

<br>

**6️⃣** **Inspect the Entities** and see if there are any **Related Events**

<br>

The Entity is involved with other **Brute Force Attempts** during the same period.

<br>

![azure portal](https://github.com/user-attachments/assets/e3e70d17-02be-40d5-9832-6c8dc61f05ff)

<br>

<br>

<h2></h2>

<br>

**7️⃣** **Determine Legitimacy** of the Incident

<br>

Determined to be ➜ a **Legitimate Incident** ✅

<br>

<h2></h2>

<br>

**8️⃣** If **True Positive** ➜ Continue | If **False Positive** ➜ Close it out

<br>

Determined to be ➜ a **True Positive** ✅

From the **Investigation** ➜ you can see that the **Attacker / Entity** ```63.143.47.155``` is also involved in **4 other Brute Force Attempt Instances**.

<br>

  </details>

<br>

<br>

## Containment, Eradication & Recovery

<br>

<details close> 
  
**<summary> 💡 Note</summary>**

<br>

I will address this later ➜ in the **Environment Hardening Section**.

Despite that ➜ I'm including the steps here for reference from the **Incident Response Playbook**.

<br>

  </details>

<br>

➡️ **Lock down the NSG** assigned to that VM / Subnet ➜ either **Entirely** or to **Only Allow Necessary Traffic**.

➡️ **Reset** the affected **User’s Password**.

➡️ **Enable MFA**

<br>

<br>

## Post-Incident Activity

<br>

✅ Document Findings and Close out the Incident in Sentinel.

<br>

<details close> 
  
**<summary> 💡 Note</summary>**

<br>

Check out the **Lessons Learned Section** for more details on this Incident.

<br>

  </details>

<br>

  </details>

<h2></h2>

<details close> 
<summary> <h2>Incident ❷ - Possible Privilege Escalation - Azure Key Vault</h2> </summary>
<br>

> <details close> 
>   
> **<summary> 💡 </summary>**
> 
> This Incident gets triggered when Sentinel detects Unusual or Unauthorized Access to Critical Credentials in Azure Key Vault.
> 
> For example ➜ when someones unauthorized reads an important Password from our Entreprise Password Manager ➜ Azure Key Vault.
> 
>   </details>

<br>

## Incident Description

<br>

➡️ This Incident involves the unexpected reading of a critical **Secret** from the organization's **Key Vault**.

<br>

<br>

## Initial Response Actions

<br>

✔ Verify the Authenticity of the Alert or Report.

✔ Identify the Secret that was read and the User or Application that read it.

✔ Determine How and When the Secret was read.

✔ Assess the Potential Impact of the Incident.

<br>

<br>

## Detection & Analysis

<details close> 
<summary> <h3>🎯 Step-by-Step</h3> </summary>

<br>
  
**1️⃣** Set the **Severity**, the **Status** & the **Owner** of the Incident:

<br>

![azure portal](https://github.com/user-attachments/assets/6dc6cf54-b40b-47f0-854b-8fbd32c7712b)

<br>

<h2></h2>

<br>

**2️⃣** **View Full Details**

<br>

![azure portal](https://github.com/user-attachments/assets/780dbef7-c579-4fd1-ae9d-7006e0d2ab53)

<br>

<h2></h2>

<br>

**3️⃣** Observe the **Activity Log**

<br>

**```Nothing to show here.```**

<br>

<h2></h2>

<br>

**4️⃣** Observe the **Entities** & **Incident Timeline**

<br>

![azure portal](https://github.com/user-attachments/assets/a5cba627-578f-4911-8a6f-400a9f48ad42)

<br>

<h2></h2>

<br>

**5️⃣** **Investigate the Incident** and continue trying to **Determine the Scope**

<br>

![azure portal](https://github.com/user-attachments/assets/7f13ccd1-e0d0-4857-90eb-c530ed56c491)

<br>

<h2></h2>

<br>

**6️⃣** **Inspect the Entities** and see if there are any Related Events

<br>

![azure portal](https://github.com/user-attachments/assets/4b6f5d37-159f-4bbb-9bee-5b0e973b02b0)

<br>

<h2></h2>

<br>

**7️⃣** **Determine Legitimacy** of the Incident

<br>

Determined **NOT** to be a **Legitimate Incident** ❌

<br>

<h2></h2>

<br>

**8️⃣** If **True Positive** ➜ Continue | If **False Positive** ➜ Close it out

<br>

Determined to be ➜ a **False Positive** ❌

<br>

  </details>

<br>

<br>

## Containment, Eradication & Recovery

<br>

➡️ None.

This was me viewing Key Vault Secrets at work ➜ I'm authorized to do this.

I don't think there is anything wrong with the Rule Logic here ➜ just happened to be a legitimate and authorized Incident-Generating Event.

<br>

<br>

## Post-Incident Activity

<br>

✅ Document Findings and Close out the Incident in Sentinel.

<br>

![azure portal](https://github.com/user-attachments/assets/b0f91414-fa5e-4414-b9da-57c238fccbb4)

<br>

<br>

  </details>

<h2></h2>

<details close> 
<summary> <h2>Incident ❸ - Brute Force SUCCESS - Microsoft Entra ID</h2> </summary>
<br>

> <details close> 
>   
> **<summary> 💡 </summary>**
> 
> The Incident gets triggered when Sentinel detects a Successful Login to a Microsoft Entra ID Account following numerous Failed Login Attempts.
> 
> For example ➜ an Attacker Successfully Accessed a Microsoft Entra ID Account by repeatedly Guessing Passwords.
> 
>   </details>

<br>

## Incident Description

<br>

➡️ This Incident involves Observation of potential **Brute Force Success against Microsoft Entra ID**.

<br>

<br>

## Initial Response Actions

<br>

✔ Verify the Authenticity of the Alert or Report.

✔ Immediately Identify and Revoke Sessions/Access for Affected User.

✔ Identify the Origin of the Attacker & Determine if they are Attacking or Involved with anything else.

✔ Assess the Potential Impact of the Incident.

✔ What Type of Account was it?

✔ What Roles did it have?

✔ How long has it been since the Breach went Unattended?

<br>

<br>

## Detection & Analysis

<details close> 
<summary> <h3>🎯 Step-by-Step</h3> </summary>

<br>
  
**4️⃣** Observe the **Entities** & **Incident Timeline**

<br>

![azure portal](https://github.com/user-attachments/assets/4316f744-c792-4cba-a7c0-e9e44b00aa3e)

<br>

<h2></h2>

<br>

**5️⃣** **Investigate the Incident** and continue trying to **Determine the Scope**

<br>

![azure portal](https://github.com/user-attachments/assets/c2aa1fce-32ac-4003-a659-a82ee50f319d)

<br>

  </details>

<br>

<br>

## Containment, Eradication & Recovery

<br>

➡️ **Reset** the affected **User’s Password & Roles** if applicable.

➡️ **Enable MFA**.

➡️ Consider preventing any logins from outside the US with **Conditional Access***.

<br>

<br>

## Post-Incident Activity

<br>

✅ Document Findings and Close out the Incident in Sentinel.

<br>

<details close> 
  
**<summary> 📝 Documentation</summary>**

<br>

This is another **False Positive** ❌

It could have been Multiple Login Attempts with the Incorrect Password or MFA Code.

I recognize this IP from work ➜ although I'm not entirely sure how 35 events were produced.

Perhaps by restoring multiple browser tabs simultaneously?
  
  - MFA is already Enabled on the User's Account.
 
  - and the Logins occurred from an Expected IP.

<br>

  </details>

<br>

![azure portal](https://github.com/user-attachments/assets/7453979b-1468-41fe-ab5e-54b7626b59aa)

<br>

<br>

  </details>

<h2></h2>

<details close> 
<summary> <h2>Incident ❹ - Brute Force ATTEMPT - Linux Syslog</h2> </summary>
<br>

> <details close> 
>   
> **<summary> 💡 </summary>**
> 
> This Incident gets triggered when Sentinel detects a series of Consecutive Failed Login Attempts on a Linux Machine, recorded in the Syslog.
> 
>   </details>

<br>

## Incident Description

<br>

➡️ This Incident involves Observation of potential **Brute Force Attempts against a Linux Virtual Machine**.

<br>

<br>

## Initial Response Actions

<br>

✔ Verify the Authenticity of the Alert or Report.

✔ Immediately Isolate the Machine & Change the Password of the Affected User.

✔ Identify the Origin of the Attacks & Determine if they are Attacking or Involved with anything else.

✔ Determine How and When the Attack occurred.

✔ Are the NSGs not being Locked Down? If so ➜ Check other NSGs.

✔ Assess the Potential Impact of the Incident.

✔ What Type of Account was it? Permissions?

<br>

<br>

## Detection & Analysis

<details close> 
<summary> <h3>🎯 Step-by-Step</h3> </summary>

<br>
  
**1️⃣** Set the **Severity**, the **Status** & the **Owner** of the Incident:

<br>

![azure portal](https://github.com/user-attachments/assets/a78aa8c6-5ab7-4229-8d69-61f8c479dc28)

<br>

<h2></h2>

<br>

**5️⃣** **Investigate the Incident** and continue trying to **Determine the Scope**

<br>

![azure portal](https://github.com/user-attachments/assets/a79b05a8-8c0a-4fec-b690-b96051203826)

<br>

![azure portal](https://github.com/user-attachments/assets/aeeb946b-3404-4f60-9a4d-1106374f07bc)

<br>

<h2></h2>

<br>

**6️⃣** **Inspect the Entities** and see if there are any **Related Events**.

<br>

![azure portal](https://github.com/user-attachments/assets/c3cbf772-7e0b-4ad2-967e-9c2b70924f57)

<br>

![azure portal](https://github.com/user-attachments/assets/478d9be9-7822-4b30-a9c5-cdfafcf5cb70)

<br>

![azure portal](https://github.com/user-attachments/assets/47a651e6-3887-42b7-bfc8-fba3ef30d281)

<br>

![azure portal](https://github.com/user-attachments/assets/3aed1986-18eb-4bfd-93d9-f358b77592a9)

<br>

![azure portal](https://github.com/user-attachments/assets/10fe187d-3898-4edf-b276-bdc4b89fe7e4)

<br>

![azure portal](https://github.com/user-attachments/assets/fadc1a2e-eb84-4f70-a48b-24dbe452c3f0)

<br>

  </details>

<br>

<br>

## Containment, Eradication & Recovery

<br>

➡️ **Lock down the NSG** assigned to that VM / Subnet ➜ either **Entirely** or to **Only Allow Necessary Traffic**.

<br>

<br>

## Post-Incident Activity

<br>

✅ Document Findings and Close out the Incident in Sentinel.

<br>

<details close> 
  
**<summary> 📝 Documentation</summary>**

<br>

There are **6 Entities** (218.92.0.118, 151.80.184.123, 123.49.33.102, 43.134.54.244, 43.156.227.146, 165.22.62.136) ➜ Attacking this Linux Virtual Machine ➜ with No Successful Attempts.

There is a total of **30 Events** grouped into **5 Alerts**.

⚠️ Suspected Over-Exposure to the Public Internet.

<br>

  </details>

<br>

![azure portal](https://github.com/user-attachments/assets/240f7483-122a-4ce0-883f-bd09c5ef7af4)

<br>

<br>

  </details>

<h2></h2>

<br>

<br>

<br>

<br>

<br>

<br>

<br>
  
<br>
