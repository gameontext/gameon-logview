# gameon-logview
A quick server logs viewer for liberty applications.. intended to be consumed as a library.

## Using the library in your Java projects

We use jitpack to build this library, which means you can direct maven or gradle directly to our github releases to satisfy dependencies.

1. include jitpack.io in your list of repositories:
  * In maven:
  ```
    <repositories>
      <repository>
        <id>jitpack.io</id>
        <url>https://jitpack.io</url>
      </repository>
    </repositories>
  ```
  * In gradle:
  ```
    repositories {
      maven { url "https://jitpack.io" }
    }
  ```
2. Include version of the library in your dependencies:
  * In maven:
  ```
    <dependency>
      <groupId>com.github.gameontext</groupId>
      <artifactId>gameon-logview</artifactId>
      <version>v1.0.0</version>
    </dependency>
  ```
  * In gradle:
  ```
    dependencies {
	    compile 'com.github.gameontext:gameon-logview:v1.0.0'
    }
  ```
  * In your `server.xml`
  ```
    <jndiEntry jndiName="logViewKey" value="myLogViewPassword"/>
  ```
    (or, if you prefer to keep the password in an environment var.. )
  ```
    <jndiEntry jndiName="logViewKey" value="${env.MAP_KEY}"/>
  ```
  
3. Use Logview to view logs from your Liberty server.

  Logview adds a servlet to the context root with the name 'LogView'
  If your content was as http://127.0.0.1/myContextRoot then you can access
  Logs via the url http://127.0.0.1/myContextRoot/LogView

4. Send Ozzy Shoes!

  https://www.amazon.ca/registry/wishlist/3OGMJ2X31EHP6
