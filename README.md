project 7 & 8   
1.(Required) Shortcodes: allow unclosed HTML elements in attributes   
  Summary: Allows malformed HTML elements to execute JS in the browser when creating or editing pages or posts using plain text editor.  
        Vulnerability types: XSS   
        Tested in version: 4.2   
        Fixed in version: 4.2.5    
        Steps to recreate: 1. Create new page with any title 2. Insert the following: TEST!!![caption width="1" caption='<a href="' ">]</a><a href="http://onMouseOver='alert(1)'">XSS 💀</a> 3. View page and mouseover to see alert    
 gif：problem 1
 Affected source： code:https://github.com/WordPress/WordPress/commit/f72b21af23da6b6d54208e5c1d65ececdaa109c8      
 2.(Required) User enumeration using wpscan     
 Summary: Due to the different login error messages, we can determine whether or not a user account exists on the WordPress install. Using wpscan we can quickly enumerate all usernames since our install does not limit log in attempts     
Vulnerability types: User Enumeration    
Tested in version: 4.2   
Fixed in version: -   
Steps to recreate: In Kali terminal run: wpscan --url http://wpdistillery.vm --enumerate u     
gif： problem 2
Affected source code: https://github.com/WordPress/WordPress/blob/4.2-branch/wp-login.php     
3.(Required) Vulnerability Name or ID     
 Summary: Using a wordlist of common passwords and enumerating the users as we did previously, we can brute force passwords and retrieve login information for any user who chooses to use an insecure password.      
Vulnerability types: Login Vulnerability     
Tested in version: 4.2    
Fixed in version: -     
Steps to recreate: In Kali terminal run wpscan --url http://wpdistillery.vm --wordlist /usr/share/wordlists/rockyou.txt --username admin      
gif： problem 3
Affected source code: https://github.com/WordPress/WordPress/blob/4.2-branch/wp-login.php    

  
