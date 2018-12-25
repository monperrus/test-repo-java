foo
foo repo in Java

1) generated repo with:

```
mvn -B archetype:generate \
    -DarchetypeGroupId=org.apache.maven.archetypes \
    -DgroupId=com.mycompany.app \
    -DartifactId=my-app
```

2) added `.travis.yml` and activated travis

3) added .gitgnore to ignore `target`

4) bump junit to 4.12

5) added env variable for GIthub authentication

```
travis encrypt GITHUB_AUTH_USER=monperrus --add
travis encrypt GITHUB_AUTH_TOKEN=eab968657466453eab --add
```

5) activated https://github.com/monperrus/gmtft

```
after_script:
  - curl -s https://www.monperrus.net/martin/gmtft.py.txt | python
```
