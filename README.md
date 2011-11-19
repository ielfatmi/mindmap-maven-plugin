Mind map maven plugin
=======

This plugin generates a MindMap from the project dependencies. The mindmap file (with the '.mm' extension) can be viewed with Freeplane (free tool).

By default, the mindmap shows the full dependency tree.
You can filter this tree at generation time by artifact's group id, by providing a parameter 'groupIdsFilteringREGEXMatch' setted with a groupId name fragment (a startswith will be performed).

Downloads
--------

The plugin is available in maven central repository:
[http://repo2.maven.org/maven2/fr/xebia/maven/plugins/mindmap-maven-plugin/](http://repo2.maven.org/maven2/fr/xebia/maven/plugins/mindmap-maven-plugin/).


Integrating with Maven's build lifecycle
--------
	
	<build>
	  <plugins>
	    <plugin>
	      <groupId>fr.xebia.maven.plugins</groupId>
	      <artifactId>mindmap-maven-plugin</artifactId>
	      <version>1.0.0</version>
	      <executions>
	        <execution>
	          <phase>package</phase>
	          <goals>
	            <goal>mindmap</goal>
	          </goals>
	        </execution>
	      </executions>
	    </plugin>
	  </plugins>
	</build>

Standalone usage examples
--------

	Usage is (for exemple) :
	mvn fr.xebia.maven.plugins:mindmap-maven-plugin:1.0.0-SNAPSHOT:mindmap

	with filtering :
	mvn fr.xebia.maven.plugins:mindmap-maven-plugin:1.0.0-SNAPSHOT:mindmap -DgroupIdsFilteringREGEXMatch=fr.xebia
	
Documentations
--------
   
    Plugin documentations:
[http://ielfatmi.github.com/mindmap-maven-plugin/plugin-info.html](http://ielfatmi.github.com/mindmap-maven-plugin/plugin-info.html).
    Maven site: 
[http://ielfatmi.github.com/mindmap-maven-plugin/](http://ielfatmi.github.com/mindmap-maven-plugin/).
    JavaDocs: 
[http://ielfatmi.github.com/mindmap-maven-plugin/apidocs/index.html](http://ielfatmi.github.com/mindmap-maven-plugin/apidocs/index.html)
	
