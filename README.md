<h1 align="center">Secure Cloud Configuration - Part 1</h1>

<br>

<h2 align="center">Regulatory Compliance: Enable NIST 800-53</h2>

<p align="center">
<img width="700" src="https://github.com/user-attachments/assets/ba44e0c3-5ee1-4d97-b92a-13e15c4c6c1e" alt="Banner"/>

<br>

<br>

In the previous labs we performed some **Incident Response**, and we even **Remediated some Vulnerabilities** like Hardening the NSGs.

We also **Captured our Environment's Traffic** in an Insecured State for 24 hours & **Recorded our Security Metrics**.

<br>

In this next step of our Project we’ll work towards **Securing our Environment**.

<br>

Basically in this lab we’re going to:

  -	Look at Microsoft Defender for Cloud’s **Secure Score**.
    
  -	Look at Microsoft Defender for Cloud’s **Recommendations**, and learn what that is.
    
  -	Enable MDC’s **Regulatory Compliance for NIST 800-53**.

<br>

>   <details close> 
>   
> **<summary> 💭 Reminder</summary>**
> 
> If you remember ➜ **NIST 800-53** is the **Security and Privacy Control Family**.
> 
> It’s basically just a really large **Catalog of Controls** that we can use to either **Evaluate** or help **Secure our Environment**.
> 
> <br>
>   
> When we Enable the **NIST 800-53 Regulatory Compliance** in **Azure**:
>   
> ➡️ It’s going to show us things that we can do in Azure to **Secure our Environment** ➜ which align with **NIST 800-53 Controls**.
> 
> It gives us a better intuition of:
>   - What is NIST 800-53.
>   - How it’s Used.
>   - Why it’s Useful.
>   
>   </details>

<br>

<br>

<details close> 
<summary> <h2>1️⃣ Inspect MDC Secure Score & Recommendations</h2> </summary>
<br>

The first thing we’re going to do is Inspect the [**Microsoft Defender for Cloud Secure Score**](https://learn.microsoft.com/en-us/defender-xdr/microsoft-secure-score?view=o365-worldwide)

We’ll go to the **Azure Portal** ➜ open **Microsoft Defender for Cloud**:

![azure portal](https://github.com/user-attachments/assets/08ab92a6-b905-431a-a3ad-37cc7f009423)

<br>

>   <details close> 
>   
> **<summary> 💡 </summary>**
> 
> Defender for Cloud provides us with a 🛡️ **Secure Score**.
> 
> It’s a single metric that we can use to gage our **Security Posture** and how good it is.
>   
>   </details>

<br>

Then we can click on the **Recommendations** blade on the left side:

![azure portal](https://github.com/user-attachments/assets/aa067180-eb69-49ce-a58a-c2755c4dec22)

<br>

The interface will show us all the things that are contributing to our Environment’s **Security Score**.

<br>

  <details close> 
  
**<summary> 💡 </summary>**

It’ll show us areas that essentially have gaps:

➡️ So we can implement things in Azure & perform some Configurations in order to make our Security Score go Up.

<br>

  </details>

<br>

![azure portal](https://github.com/user-attachments/assets/40fd5b5b-75d8-4f88-93dc-3fb5acf65eb4)

<br>

🔍 We can look through all the different **Recommendations** and get a good sense of what we can do to **Harden our Environment**.

<br>

<h2></h2>
<br>

<h3>Inspect MDC Recommendations</h3>

<br>

If we click on ```View recommendations >```:

![azure portal](https://github.com/user-attachments/assets/fb6bf830-e0b1-445f-9a64-77f6983bc2c0)

<br>

It'll show all the things that are contributing to our **Secure Score** ➜ areas in our Environment that essentially have "Gaps".

![azure portal](https://github.com/user-attachments/assets/f1ade39b-9c81-487b-82ce-e8ce851bfe5d)

<br>

We can implent things in **Azure** ➜ make some Configurations to get our **Secure Score** to go Up.

For example: under ```> Restrict unauthorized network access``` ➜ if we click on the first Recommendation:

![azure portal](https://github.com/user-attachments/assets/04a75668-ffb7-492f-be99-88b53cca10c6)

<br>

MDC will give us Recommendations on how we can fix it:

- There's a detailed **Description** of what the Recomendation involves.
  
- And there's also the **Remediation Steps** section that breaks down what we have do to Remediate the issue.

![azure portal](https://github.com/user-attachments/assets/ed0fc54d-4774-422b-9fff-d4f379a02a76)

<br>

✅ So we've analysed the **Recommendations** that when fixed would improve our Environmen's **Secure Score**.

<br>

  </details>

<h2></h2>

<details close> 
<summary> <h2>2️⃣ Enable NIST 800-53</h2> </summary>
<br>

> Add [**NIST 800-53: Security and Privacy Controls for Information Systems and Organizations**](https://csrc.nist.gov/pubs/sp/800/53/r5/upd1/final) to **Microsoft Defender for Cloud**.
> 
> 💡 [**Full Publication**](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-53r5.pdf).

<br>

The next thing we’re going to do is **Enable Regulatory Compliance for NIST 800-53**.

This will basically do the same thing as the **MDC Secure Score Recommendations** ➜ but it’ll do it in the “lens” of **NIST 800-53**.

<br>

  <details close> 
  
**<summary> 📌 Refresher</summary>**

<br>

[NIST 800-53](https://csrc.nist.gov/projects/cprt/catalog#/cprt/framework/version/SP_800_53_5_1_0/home) is a really large control catalog with a lot of different control families like:

-	 Access Control
-	 Identification and Authentication
-	 Incidence Response, etc.

![azure portal](https://github.com/user-attachments/assets/c252a0a1-7952-41a2-8ef2-539f45ddcefa)

<br>

These are all different categories ➜ and then inside of these there’s a lot of **Sub-Controls** essentially

For example: inside of **"SC - SYSTEM AND COMMUNICATION PROTECTION"** ➜ there's a lot of different Categories:

![azure portal](https://github.com/user-attachments/assets/5126055b-5f4b-4456-9aba-62efb764c7e1)

<br>

When we enable NIST 800-53 Regulatory Compliance inside of Defender for Cloud:

  - It’s basically going to look at all the different Controls inside of NIST 800-53
    
  - And it'll suggest different things we can do in our Environment that align with, for example, SC-7:

![azure portal](https://github.com/user-attachments/assets/1d95d567-d4ed-4ef9-9c4b-6a65a3cf5c89)

<br>

Essentially it will suggest different implementations we can do in Azure to bring our Environment "Up to Par" with NIST 800-53.

In a way, show us Gaps in relation to Controls that exist in NIST 800-53.

  </details>

<br>

To add NIST 800-53:

  - First inside the MDC home page ➜ click on the **Regulatory Compliance** blade on the left side:
![azure portal](https://github.com/user-attachments/assets/5072ca93-f076-4163-80c2-967704432b2f)

<br>

  - Then at the top ➜ click on **Manage compliance policies**:

![azure portal](https://github.com/user-attachments/assets/67f38c0f-4c42-4080-8e07-d4a3db87e06d)

<br>

  - We'll then click on our ```Azure subscription 1```:

![azure portal](https://github.com/user-attachments/assets/44cef131-d6fe-4065-918b-d009306265d7)

<br>

  - Inside the **Security policy** blade ➜ under **Industry & regulatory standards**  ➜ click on the **"Add more standards"** button:

![azure portal](https://github.com/user-attachments/assets/80d7228c-709e-46e2-981b-37028c7a5374)

<br>

  - Add ```NIST 800-53 R5``` as a **Regulatory Compliance Standard**:

![azure portal](https://github.com/user-attachments/assets/f66d02b4-3cb0-40f1-aa86-91f56bdc8263)

<br>

- We'll leave the Initiative Assignment Configurations as the default ones ➜ so just click **"Create"**

![azure portal](https://github.com/user-attachments/assets/29baa074-9bbf-444f-a9b4-8a25ebf31d8e)

<br>

The Policy Initiative Assignment takes a few minutes to take effect.

After waiting a while ➜ we can confirm that **NIST 800-53 R5** was successfully assigned to our Subscription ✅

![azure portal](https://github.com/user-attachments/assets/28fedd9f-d9c4-4c85-96ae-75f482a76827)

<br>


⚠️ Again ➜ it takes some time for the policy to be added to our Environment.

But eventually it should appear inside of our MDC Dashboard ➜ under **Regulatory compliance**:

![azure portal](https://github.com/user-attachments/assets/d75d993f-2264-4122-98a5-1b36ebc9f5b9)

<br>


  <details close> 
  
**<summary> 📝 Recap</summary>**

Basically **NIST 800-53** contains a whole bunch of **Control Families** with different Controls that we can apply to our Environment.

NIST 800-53 is not specific to any Environment ➜ they're just generalized Controls.

But Microsoft created this NIST 800-53 Policy to map those General Controls to things that we can actually do inside of **Azure**.

This are the general **Control Families** defined by **NIST**:

![azure portal](https://github.com/user-attachments/assets/66c76459-949a-4f33-880b-c9d878f13baf)

<br>

If we expand one of the Control Families ➜ **“AC. Access Control”** for example:

It shows what we can do inside of the Azure Portal to our Resources to be **“Compliant”** with each individual Sub-Control:

![azure portal](https://github.com/user-attachments/assets/09b96474-e6de-4a32-b7a9-6323467736db)

<br>

Again as an example: for **IR-6(2)** as defined by NIST ➜ there could be some Improvements made in our Environment:

![azure portal](https://github.com/user-attachments/assets/eeebf9e4-d92f-4f3d-8855-9dcc1c853c7d)

<br>

We can click on the first **Automated assessment** ➜ and MDC will give us Instructions on how to remediate this issue:

If we expand the ```∨ Remediation steps``` ➜ it'll give us the Steps to Take in order to Manually Remidiate this Sub-Control.

![azure portal](https://github.com/user-attachments/assets/573f186d-db6b-45c2-bc91-e425a4433845)

<br>

  </details>

<br>

➡️ In our upcoming lab ➜ we're going to implement **SC-7 Boundary Protection**, in order to bring this Control "Up to Compliance".

<br>

<h2></h2>

  </details>

<br>

<br>

<br>

<br>

<h1>Summary</h1>
<br>

In this lab we Enabled NIST 800-53 Regulatory Compliance Policy.

Basically when we did that ➜ Azure looked at our entire Environment and compared it to NIST 800-53 General Control Families:

<br>

<p align="center">
<img width="600" src="https://github.com/user-attachments/assets/52efb6c2-59e0-4025-a9c9-ef8f298032d8" alt="Banner"/>

<br>

<br>

In doing so, it essentially found all the weak spots in our Environment that could be addressed by the **NIST 800-53 Control Catalog**.

And in the next lab we'll start remediating a few of these **Compliance Controls**.


<br>

<br>

<br>

<br>

<br>

<br>

<br>
  
<br>
