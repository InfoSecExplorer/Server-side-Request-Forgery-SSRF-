# What is Server-side Request Forgery (SSRF)?

Server-Side Request Forgery (SSRF) is a type of web application vulnerability that allows an attacker to send arbitrary HTTP requests from a vulnerable web application to an external server. The application may be tricked into sending malicious requests to internal systems, which could lead to sensitive data exposure or other security issues.

SSRF vulnerabilities occur when an application is designed to forward a user-supplied URL or other input to an external server, without properly validating or sanitizing the input. This can allow an attacker to craft a request that causes the application to send a request to an internal system or resource that would otherwise be inaccessible. For example, an attacker could use SSRF to access internal network resources such as databases, file servers, or other sensitive systems.

# General methodology and checklist for testing for SSRF vulnerabilities

**SSRF vulnerabilities typically involves the following steps**

1. Identify potential inputs that are used to construct URLs or initiate requests to external servers. These inputs may include GET or POST parameters, headers, and other user-supplied data.

2. Test each input by providing a variety of different URLs or IP addresses as the input, including internal resources, localhost, and other special values.

3. Observe the application’s behavior when provided with different inputs, and look for signs of SSRF vulnerabilities, such as the ability to access internal resources or exfiltrate data.

4. Document any vulnerabilities found, including the input that was used to trigger the vulnerability, the type of vulnerability, and the potential impact.

**A checklist for testing for SSRF vulnerabilities**

1. Verify if the application makes HTTP requests to user-supplied URLs

2. Verify if the application makes HTTP requests to user-supplied IP addresses

3. Verify if the application makes HTTP requests with user-supplied headers and/or cookies

4. Verify if the application makes HTTP requests to internal resources or localhost

5. Check if the application has any protection mechanisms against SSRF attacks (e.g. whitelisting allowed URLs)

6. Test if it’s possible to use the SSRF vulnerability to gain access to internal resources or steal sensitive data

7. Test if it’s possible to use the SSRF vulnerability to perform out-of-band data exfiltration

8. Test if it’s possible to use the SSRF vulnerability to perform internal port scanning

9. Test if it’s possible to use the SSRF vulnerability to bypass access controls

10. Test if it’s possible to use the SSRF vulnerability to exploit other vulnerabilities






