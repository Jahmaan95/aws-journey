**1. Error Description**  
When testing to see how the site looked the style did not come through as expected
![Screenshot 2025-06-12 191321](https://github.com/user-attachments/assets/30b7df6c-4231-4fb8-b060-35fe955a7b27)  

**2.Error/issue remediation**  
The Index.html file did not link to the styles.css because there was a typo in the file name.  

**3. Steps to reproduce**  
1. Renamed the style.css to "styles.css"
2. Re-uploaded the file to S3 bucket
3. Re-tested the public link

**4. Result**  
The website style now appears as expected.  
![Website](https://github.com/user-attachments/assets/afe85f9f-0d24-4cef-aa47-c32ff3a2043a)

