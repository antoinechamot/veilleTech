# Codecow


## Setup cobertura
```
<dependency>
    <groupId>org.codehaus.mojo</groupId>
    <artifactId>cobertura-maven-plugin</artifactId>
    <version>2.7</version>
	<configuration>
		<formats>
			<format>html</format>
			<format>xml</format>
		</formats>
		<check />
	</configuration>
</dependency>
```

## Integrate with Circle CI
```
 - run: mvn integration-test cobertura:cobertura
 - run:
	name: Send to CodeCov
	command: bash <(curl -s https://codecov.io/bash)
```

## Resources

https://codecov.io