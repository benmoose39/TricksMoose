[🔙 cd $HOME](https://benmoose39.github.io/TricksMoose)

<h1>Switching between different Java versions</h1>
<p><i>There can be situations when we need to switch between java versions. Here I showcase a method where you can switch between different versions of java in <b>ubuntu</b> and <b>kali</b>.
  </i></p>

### hello
<h2> The easy way </h2>
  
`sudo apt install openjdk-8-jre` (Ubuntu)
  
`sudo update--alternatives --config java`
  and choose the required version
  
> ![image](https://user-images.githubusercontent.com/29022864/132997133-9ca76672-f292-41af-9689-57f406c052ac.png)



<h2> The hard way 😁 </h2>
<h4>Switching from 1.1x.x to 1.8.0</h4>
- Check the version with:

> `java -version`
![image](https://user-images.githubusercontent.com/29022864/132988214-e55aab98-94b1-4efe-aeca-8556b72393c5.png)

- See where the binary is linked to:

> `ls -l $(which java)`
![image](https://user-images.githubusercontent.com/29022864/132993428-4e8ffa02-2b64-4c78-88c3-67121088d14a.png)
Here it is linked to ```/etc/alternatives/java```
`ls -l /etc/alternatives/java`
![image](https://user-images.githubusercontent.com/29022864/132994734-6ebf383b-4325-45ad-80a2-1af023357b15.png)

- `cd /usr/lib/jvm/` and list the files:

> ![image](https://user-images.githubusercontent.com/29022864/132994794-8db218c8-7cfd-4b80-9541-f49bde558ff3.png)
The only version we see here is 1.14.0

- Install java-1.8.0 with:
  
`sudo apt install openjdk-8-jre` (Ubuntu)
  
`sudo apt install nvidia-openjdk-8-jre` (Kali)

> `ls -la`
![image](https://user-images.githubusercontent.com/29022864/132994979-3431b59b-f9d9-4c88-babd-929832dca8e6.png)
`cd java-1.8.0-openjdk-amd64/jre/bin && ls -l`
![image](https://user-images.githubusercontent.com/29022864/132995164-0f1a55ea-ead6-4a18-aecf-30845f20820d.png)
Checking the version of this binary:
![image](https://user-images.githubusercontent.com/29022864/132995456-0e1f734c-a4a8-4360-a36f-4bb3c9ad8e44.png)

- Now link this java to /etc/alternatives/java:

> `ln -sf $(pwd)/java /etc/alternatives/java`
![image](https://user-images.githubusercontent.com/29022864/132995971-e98cee10-0c03-46f5-90ae-eb331afc2668.png)

