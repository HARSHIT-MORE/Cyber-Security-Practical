--------------------------------------------------Practical 1: Network Reconnaissance and Exposure Analysis----------------------------------------

Task1: Check Local network state
        ipconfig /all
        What is My IP

TASK 2: Test Network Connectivity
          ping -n 10 10.25.1.4 (default gateway)
          ping -n 10 8.8.8.8
          ping -n 10 google.com

TASK 3: Comparative Route Analysis
        tracert google.com (1st hop = router ,2nd hop = ISP,3rd hop = final destination IP )
        tracert instagram.com
        tracert flipkart.com

TASK 4: DNS footprint analysis
      nslookup www.google.com  
      nslookup iitb.ac.in

--------------------------------------------------PRACTICAL 2 : Passive OSINT and External Exposure Analysis----------------------------------------------------------

TASK 1: WHOIS/RDAP Analysis
      WHOis - du.ac.in , ntpc.co.in , flipkart.com

TASK 2: (a) Shodan-based Exposure Assessment
          Ref: https://www.shodan.io/search/examples
          - Apache, flipkart.com

Task 2(b) Interpreting India’s Internet Exposure using Shodan Observatory
          https://exposure.shodan.io/#/IN

TASK 3: Certificate Transparency Lookup and Subdomain Intelligence
        Visit crt.sh -- %du.ac.in

---------------------------------------------- ASSIGNMENT ----------------------------------------------------------------------

Task 1: Sending an encrypted email
        Flowcrypt -- RSA 3072 key pair

Task 2: Website Cloning, Phishing and Credential Harvesting using SET
        sudo setoolkit
        ....
        ip addr show eth0 | grep 'inet '  -- (this is where captured credentials will be sent)
        URL: https://bwapp.hakhub.net/login.php
        Run local host and side by side this url
        Inspect and notice the form tag
        Now go to network and see the POST request 

C. Credential Harvesting Demonstration



--------------------------------- PRACTICAL 3 : Phishing Email Analysis ----------------------------------------------------------

Task 1: Finding the Full Email Header
        Gmail -> Open any mail -> show original 

Task 2: Analyse the email in the EML Analyser

Task 3: Header analysis with MX Toolbox

Task 4: Tracing the Originating IP Address and analysing its reputation
        Note the x-originating-ip address from your MX Toolbox analysis.
        IP in VirusTotal, AbusePDB, and/or Cisco Talos

Task 5 - domain ownership and URL/Domain analysis
          Run WHOIS for:
                o atendimento.com.br
                o blog1seguimentmydomaine2bra.me
        Submit the extracted URL to urlscan.io and/or VirusTotal URL analysis.



-------------------------------- PRACTICAL 4: GOOGLE DORKING -----------------------------------------------------------------------

Task 1: Basic Search Operator Practice
        navigate to: https://www.google.com
        site:bbc.co.uk intitle: "news"
        site:bbc.co.uk intitle:"sport"

Task 2: Finding Exposed Files & Systems
        intitle:"index of" site:edu filetype:xls
        inurl:"/wp-admin/admin-ajax.php"
        filetype:env "DB_PASSWORD"
        site:github.com "api_key" OR "secret_key"

Task 3: Google Hacking Database (GHDB)
        https://www.exploit-db.com/google-hacking-database
        inurl:.com index of movies  --> Vulnerable File
        intitle:"index of"site:.gov.in  -> Web Server Detection
        intitle: index of/concrete/Password -> Sensitive Directories


----------------------------- PRACTICAL 5: Malware Analysis ----------------------------------------------------------------------

Task: Static Malware Analysis using Free Online Tools
    --  Download the EICAR test file from Download Anti Malware Testfile -EICAR. Save it to your Downloads folder as eicar.com.txt.Confirm your operating system and antivirus settings allow temporary access to the file
    --  Compute hash value : Get-FileHash -Algorithm SHA256 "C:Users\Asus\Download\eicar.com.txt"
    --  Submit the SHA256 hash (not the file) to VirusTotal at VirusTotal and check Detection.
    -- Open the file in Hexed.it (HexEd.it)
    --  CyberChef (CyberChef) with the From Base64 


          
