<h1>Selection Process Overview</h1>
    <p>The selection process will focus on identifying mechanisms that are best suited for the project, considering both passive and active reconnaissance tools. The criteria for selection will be centered on host discovery, network sniffing, and Open Source Intelligence (OSINT) ensuring the most efficient and effective utilization of resources.</p>
    <h2>Selection Criteria</h2>
    <p>Considerations include but are not limited to:</p>
    <ul>
        <li>Login portals</li>
        <li>Public records</li>
        <li>DNS records</li>
        <li>Search engines</li>
        <li>SSL Certificate Information</li>
        <li>Cryptographic measures</li>
         <li>Hidden Files/Directories</li>
    </ul>
     <h1>Penetration Testing Tools Overview</h1>
    <table>
        <tr>
            <th>Tool</th>
            <th>How It Works</th>
            <th>Key Findings</th>
        </tr>
        <tr>
            <td>Shodan</td>
            <td>Searches for devices connected to the internet.</td>
            <td>Exposed devices and services.</td>
        </tr>
        <tr>
            <td>DNSDumpster</td>
            <td>Discovers DNS servers and records.</td>
            <td>DNS mappings and domain related endpoints.</td>
        </tr>
        <tr>
            <td>Censys</td>
            <td>Scans the internet for information about hosts and networks.</td>
            <td>Visible network assets and their configurations.</td>
        </tr>
        <tr>
            <td>Maltego</td>
            <td>Provides graphical link analysis for digital forensics.</td>
            <td>Relationships between pieces of information from various sources.</td>
        </tr>
        <tr>
            <td>Hunter</td>
            <td>Finds email addresses associated with a domain.</td>
            <td>Email addresses and their ties to organizations.</td>
        </tr>
        <tr>
            <td>DirBuster</td>
            <td>Brute forces directories and file names on web servers.</td>
            <td>Hidden files and directories on a web server.</td>
        </tr>
        <tr>
            <td>Nmap</td>
            <td>Network discovery and security auditing.</td>
            <td>Open ports, services, and system details.</td>
        </tr>
        <tr>
            <td>SSL Scan</td>
            <td>Assesses the SSL/TLS security posture of a target.</td>
            <td>SSL/TLS vulnerabilities and configurations.</td>
        </tr>
        <tr>
            <td>VirusTotal</td>
            <td>Aggregates multiple antivirus products and online scan engines to check for viruses.</td>
            <td>Malicious files, URLs, and software detection.</td>
        </tr>
    </table>
     <h1>Commands for Target Analysis</h1>
    <h2>Nmap</h2>
    <p><strong>Basic Scan:</strong> Checks for open ports and running services.</p>
    <br>
    <code>nmap -sV "target"</code>  <br>
    <br>
    <p><strong>Aggressive Scan:</strong> performs a fast, comprehensive scan on all TCP ports of a specified target, identifying services, versions, operating systems, and more, with the results saved to a .txt file.</p>
    <br>
    <code>nmap -sS -A -T4 -O -sV -p- -oN target.txt "target"</code>
    <br>
    <h2>Shodan</h2>
    <p>Use the Shodan CLI to search for information about an IP, assuming you have the API key.</p>
    <code>shodan host "target"</code>  <br>
    
<br>
    
![shodan1](https://github.com/jcpio00/External_Reconnaissance_Playbook/assets/72210067/001f9a86-1e0b-4e28-9c03-b3615e268410)

<br>
    <h2>Censys</h2>
    <p>Using the Censys CLI, an example command for searching IP information, with API key:</p>
    <br>
    <code>censys search "target"</code><br>
<br>

<img width="1013" alt="censys2" src="https://github.com/jcpio00/External_Reconnaissance_Playbook/assets/72210067/39c2d5e5-d684-4211-8ca4-a4903848a7a6">

<br>
    <h2>SSL Scan</h2>
    <p>Checks the SSL/TLS certificates and configurations of services running on the default HTTPS port.</p>
    <br>
    <code>sslscan "target"</code>
    <br>
    <h2>VirusTotal</h2>
    <p>Used to check for any associated domains, URLs, or files reported as malicious, typically through the web interface or API.</p>
<br>

![virustotal](https://github.com/jcpio00/External_Reconnaissance_Playbook/assets/72210067/38457cd7-f664-4d92-b1d3-25d84d5b5150)


<br>
    <h3>Note on Maltego, Hunter, and DNSDumpster</h3>
    <p>These tools are more oriented towards domain names and email addresses rather than direct IP address interrogation.</p>
    <h3>Maltego</h3>
    <p>Use the Maltego application to visually map relationships. Example transforms are initiated via the GUI.</p>
<br>

![maltego](https://github.com/jcpio00/External_Reconnaissance_Playbook/assets/72210067/e4760a9a-589d-49b6-b5f8-95fb65408863)


<br>
    <h3>Hunter</h3>
    <p>Access through the web interface and enter the domain to search for email addresses associated with it.</p>
<br>

![hunter](https://github.com/jcpio00/External_Reconnaissance_Playbook/assets/72210067/862f0c95-1947-4b2c-b010-c241b8419ac8)


<br>
    <h3>DNSDumpster</h3>
    <p>Access through the web interface and enter the domain to find DNS records.</p>
<br>

![dnsdumpster](https://github.com/jcpio00/External_Reconnaissance_Playbook/assets/72210067/e2aaf935-87c0-49eb-94df-3add5f5b9ba2)


<br>
    <h2>DirBuster</h2>
    <p>DirBuster is designed to find directories and files on web servers. It is more about configuring and running the tool through its interface for web servers running on the IP address.</p>
<br>

![dirbuster](https://github.com/jcpio00/External_Reconnaissance_Playbook/assets/72210067/b333371c-2ca6-4ca1-b358-c4e5c51450f8)


<br>
    <p><em>Always ensure that your usage of these tools is authorized and ethical to avoid legal repercussions.</em></p>

   

    
