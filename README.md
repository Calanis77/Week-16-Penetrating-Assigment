## Week 16 Homework Submission File: Penetration Testing 1

#### Step 1: Google Dorking


- Using Google, can you identify who the Chief Executive Officer of Altoro Mutual is:
  - I found from the website that Karl Fitzgerald is the CEO

- How can this information be helpful to an attacker:
  - This information is useful to an attacker who wants to send phishing email directly to the executive members.

#### Step 2: DNS and Domain Discovery

Enter the IP address for `demo.testfire.net` into Domain Dossier and answer the following questions based on the results:

  1. Where is the company located: 
    - Sunnyvale, CA. 94085

  2. What is the NetRange IP address:
    - "65.61.137.64 - 65.61.137.127"

  3. What is the company they use to store their infrastructure:
    - CustName:       Rackspace Backbone Engineering
Address:        9725 Datapoint Drive, Suite 100
City:           San Antonio
StateProv:      TX
PostalCode:     78229
Country:        US
RegDate:        2015-06-08
Updated:        2015-06-08
Ref:            https://rdap.arin.net/registry/entity/C05762718
  4. What is the IP address of the DNS server:
    - "65.61.137.117"
#### Step 3: Shodan

- What open ports and running services did Shodan find:
  - Open Ports on IP "65.61.137.117" are (80, 443, 8080)

#### Step 4: Recon-ng

- Install the Recon module `xssed`. 
  - marketplace install xssed
    keys add shodan_api tbmKjcV0ont04nJMTcEuBsmnDQtzLFhe
    modules load recon/domains-vulnerablilities/xssed
- Set the source to `demo.testfire.net`. 
  - options set SOURCE demo.testfire.net
- Run the module. 
  - run

Is Altoro Mutual vulnerable to XSS: 
  - Yes, 1 total (1 new) vulnerability found.

### Step 5: Zenmap

Your client has asked that you help identify any vulnerabilities with their file-sharing server. Using the Metasploitable machine to act as your client's server, complete the following:

- Command for Zenmap to run a service scan against the Metasploitable machine: 
  - Start Metasploitable 
  - Type zenmap in the Kali command line
  - Target "192.168.0.10"
  - On Profile click on Quick Scan
  - Click on Scan 
 
- Bonus command to output results into a new text file named `zenmapscan.txt`:

- Zenmap vulnerability script command:
  - Click on the Profile tab
  - Click on Edit Selected Profile
  - Click on Scripting Tab
  - Scrowl down till you see any options starting with 'ftp'
  - Select 'ftp-vsftpd-backdoor' 
  - Click on Save Changes.

- Once you have identified this vulnerability, answer the following questions for your client:
  1. What is the vulnerability:

  2. Why is it dangerous:

  3. What mitigation strategies can you recommendations for the client to protect their server:

---
© 2020 Trilogy Education Services, a 2U, Inc. brand. All Rights Reserved.  
