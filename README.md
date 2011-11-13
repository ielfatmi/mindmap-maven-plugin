Mind map maven plugin
=======
This plugin generates a MindMap from the project dependencies. The mindmap file (with the '.mm' extension) can be viewed with Freeplane (free tool).

By default, the mindmap shows the full dependency tree.
You can filter this tree at generation time by artifact's group id, by providing a parameter 'groupIdsFilteringREGEXMatch' setted with a groupId name fragment (a startswith will be performed).

Usage is (for exemple) :
mvn fr.xebia.maven.plugins:mindmap-maven-plugin:1.0.0-SNAPSHOT:mindmap

with filtering :
mvn fr.xebia.maven.plugins:mindmap-maven-plugin:1.0.0-SNAPSHOT:mindmap -DgroupIdsFilteringREGEXMatch=fr.xebia