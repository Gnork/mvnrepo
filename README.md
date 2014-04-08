mvnrepo
=======

# refer to this repository in project pom.xml
<repositories>
	<repository>
		<id>Gnork-snapshots</id>
		<url>https://raw.github.com/Gnork/mvnrepo/master/snapshots</url>
		<releases>
			<enabled>false</enabled>
		</releases>
		<snapshots>
			<enabled>true</enabled>
		</snapshots>
	</repository>
	<repository>
		<id>Gnork-releases</id>
		<releases>
			<enabled>true</enabled>
		</releases>
		<snapshots>
			<enabled>false</enabled>
		</snapshots>
		<url>https://raw.github.com/Gnork/mvnrepo/master/releases</url>
	</repository>
</repositories>

# add maven artifact to this repository
1. clone repository
2. run the following command for desired artifact:
mvn deploy:deploy-file -DgroupId=com.syvys -DartifactId=jaRBM -Dversion=1.1 -Dpackaging=jar -Dfile=/filelocation/jaRBM_v1.1.jar -Durl=file:/pathToRepository/mvnrepo/releases
3. add, commit, push
