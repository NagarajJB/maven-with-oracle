
# Configure maven master password - Encrypt master password
	mvn --encrypt-master-password
# m2/security-settings.xml	
	<settingsSecurity>
		<master>{abcdencryptedpassword}</master>
	</settingsSecurity>

# Add to m2/settings.xml for Oracle
	mvn --encrypt-password
# Password edited to be wrong though encrypted

	<server>
		<id>maven.oracle.com</id>
		<username>mail2njb@gmail.com</username>
		<password>{abcdencryptedpassword}</password>
		<configuration>
		  <basicAuthScope>
			<host>ANY</host>
			<port>ANY</port>
			<realm>OAM 11g</realm>
		  </basicAuthScope>
		  <httpConfiguration>
			<all>
			  <params>
				<property>
				  <name>http.protocol.allow-circular-redirects</name>
				  <value>%b,true</value>
				</property>
			  </params>
			</all>
		  </httpConfiguration>
		</configuration>
	</server>





# Add to m2/settings.xml for PackageCloud
Use tokens from PackageCloud

	<server>
      <id>packagecloud.release</id>
      <password>8f7f2a49eaeasdawrong68359bf3518c1f5f15280c0</password>
    </server>
	
    <server>
      <id>packagecloud.snapshot</id>
      <password>8f7f2a49eaeasdawrong68359bf3518c1f5f15280c0</password>
    </server>
	
