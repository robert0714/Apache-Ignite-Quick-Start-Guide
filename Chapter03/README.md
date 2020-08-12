# Chapter 3
## Projects
 =============================
 * Hello-world -> Datagrid basics
 * DataGrid -> Hibernate L2 caching 
 * Session-clustering -> Web Session-clustering

## Usage
 =============================
 
 ```shell
 gradle  clean install  --stacktrace
 ```
 
  ```shell
 mvn  clean  package
 ```

## LGPL Dependencies
 =============================  
[reference](https://apacheignite.readme.io/docs/maven-setup#section-lgpl-dependencies)   
The following Ignite modules have LGPL dependencies and therefore can't be deployed on Maven Central repository:

* ignite-hibernate  
* ignite-geospatial  
* ignite-schedule  

To use these modules, you will need to build them from sources manually and add them to your project. For example, to install *ignite-hibernate* into your local repository, run this command in the Ignite source package:

Shell
```
git clone https://github.com/apache/ignite.git
cd  ignite
git checkout 2.8.1
mvn clean install -Dfile.encoding=UTF-8 -Dproject.build.sourceEncoding=UTF-8  -DskipTests -Dfile.encoding=UTF-8 -Plgpl -pl modules/hibernate-5.1 -am 
```
Please do not use ibm jdk