# MapStruct

## What is MapStruct ?

It is a code generator for Java bean mapping
 -> Help reduce coding for type conversions


Used for DTO


Others mapping frameworks : Dozer,Orika,ModelMapper,JMapper


## Example

@Mapper(componentModel="spring")
public interface CategoryMapper {
	
	CategoryMapper INSTANCE = Mappers.getMapper(CategoryMapper.class);
	
	CategoryDTO categoryToCategoryDTO(Category category);

}


<dependency>
	<groupId>org.mapstruct</groupId>
	<artifactId>mapstruct-jdk8</artifactId>
	<version>1.3.0.Final</version>
</dependency>


<plugin>
	<groupId>org.apache.maven.plugins</groupId>
	<artifactId>maven-compiler-plugin</artifactId>
	<configuration>
		<annotationProcessorPaths>
			<path>
					<groupId>org.projectlombok</groupId>
					<artifactId>lombok</artifactId>
					<version>${lombok.version}</version>
			</path>
			<path>
					<groupId>org.mapstruct</groupId>
					<artifactId>mapstruct-processor</artifactId>
					<version>1.3.0.Final</version>
			</path>
		</annotationProcessorPaths>
	</configuration>
</plugin>