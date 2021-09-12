[cd $HOME](https://benmoose39.github.io/TricksMoose)

<h1>Changing Java versions</h1>
<p><i>There can be situations when we need to switch between java versions. Here I showcase a method where you can switch between different versions of java in <b>ubuntu</b> and <b>kali</b>.
  </i></p>

<h3>Ubuntu- Switching from 1.14.0 to 1.8.0</h3>
- Check the version with:
> `java -version`
![image](https://user-images.githubusercontent.com/29022864/132988214-e55aab98-94b1-4efe-aeca-8556b72393c5.png)

- See where the binary is linked to:
> `ls -l $(which java)`
