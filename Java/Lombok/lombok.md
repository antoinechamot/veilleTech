# Lombok

## What is lombok ?

- Project that brings very simple annotations to add in common things like getters and setters,
  builder, loggers .....
  
## How works ?

- Hooks in via Annotation processor API
- The raw source code is passed to Lombok for code generation before java continues
- Produces properly compiled Java code in conjunction with the Java compiler
  
## Avantages ?

- Simplify development : Cuts down a lot of boilerplate code
- make your POJOs concise as it will hide the parts that are not that important

## Problems  ?

- Since source files are not changed some old IDE can be confused => may required plugin install


## Features

- @Getter,@Setter,@ToString,@EqualsAndHashCode,@NoArgsConstructor,@RequiredArgsConstructor,
  @Data,@Value,@NonNull,@Builder, @SneakyThrows, @Synchronized,@Log,@Slf4l

## Resources
- https://projectlombok.org/
- https://mvnrepository.com/artifact/org.projectlombok/lombok


