# 41. XSS
## What is XSS?
Cross site scripting (XSS) is an attack in which an attacker injects malicious executable scripts into the code of a trusted application or website. Attackers often initiate an XSS attack by sending a malicious link to a user and enticing the user to click it. If the app or website lacks proper data sanitization, the malicious link executes the attacker’s chosen code on the user’s system. As a result, the attacker can steal the user’s active session cookie.

## How Does Cross Site Scripting Work?
XSS is an injection attack that exploits the fact that browsers cannot differentiate between valid scripts and attacker-controlled scripts. XSS attacks bypass the same-origin policy, which is designed to prevent scripts that originate in one website from interacting with other scripts from different websites.

When the same-origin policy is not properly enforced, attackers can inject a script that modifies the web page. For example, the script can allow an attacker to impersonate a pre-authenticated user. It also allows attackers to input malicious code, which is then executed by the browser, or execute JavaScript that modifies content on the page.

XSS can cause serious issues. Attackers often leverage XSS to steal session cookies and impersonate the user. Attackers can also use XSS to deface websites, spread malware, phish for user credentials, support social engineering techniques, and more.

## What Languages are Targets of XSS?
Unsanitized user input can put any web application at risk of an XSS attack. The most common language for XSS attacks is JavaScript, but XSS can affect HTML, Flash, VBScript, CSS, and other web development languages and frameworks.

## What is the Impact of XSS?
Cross site scripting attacks can have devastating consequences. Code injected into a vulnerable application can exfiltrate data or install malware on the user’s machine. Attackers can masquerade as authorized users via session cookies, allowing them to perform any action allowed by the user account.

XSS can also impact a business’s reputation. An attacker can deface a corporate website by altering its content, thereby damaging the company’s image or spreading misinformation. A hacker can also change the instructions given to users who visit the target website, misdirecting their behavior. This scenario is particularly dangerous if the target is a government website or provides vital resources in times of crisis.

## How can you avoid XSS vulnerabilities?
It’s important to implement security measures early in the application’s development life cycle. For example, carry out software design phase security activities such as architecture risk analysis and threat modeling. It is equally important to conduct security testing once application development is complete.
## Resources
https://brightsec.com/blog/xss/

https://www.geeksforgeeks.org/what-is-cross-site-scripting-xss/?ref=rp

https://developer.mozilla.org/en-US/docs/Glossary/Cross-

https://www.synopsys.com/glossary/what-is-cross-site-scripting.html



