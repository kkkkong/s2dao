# S2Dao

S2Dao is a Java library from the Seasar project that provides Data Access Object (DAO) infrastructure, SQL file parsing, metadata management, and result mapping for Seasar-style applications.

## Key features

- DAO metadata and convention-based mapping (DaoMetaData, BeanMetaData)
- SQL file parsing and tokenization (SqlParser, SqlTokenizer)
- ResultSet -> bean mapping (RowCreator, ResultSetHandlerFactory)
- Support for stored procedures and identifier generation
- Test support using embedded databases (HSQLDB, Derby, H2)

## Modules

- s2-dao — core library (implementation of DAO, SQL parsing, metadata, mapping)
- s2-dao-examples — example projects that demonstrate usage of s2-dao
- s2-dao-s24-test — compatibility tests for Seasar 2.4.x

## Quick start

Requirements:
- JDK with Maven support. The project was historically compiled for Java 1.4; modern JDKs can be used but you may need to set compatibility options.

Build and install locally:

```bash
# from repository root
mvn clean install

# or skip tests if you don't want to run older test suites
mvn -DskipTests clean install
```

After installation you can add the s2-dao artifact to your application's pom.xml (use the matching version found in the top-level pom).

## Running tests

The module tests use embedded databases and test resources included in the repository (data-hsqldb, data-derby, data-h2). To run the test suite:

```bash
mvn test
```

If tests fail on a modern JDK because of legacy source/target levels, try building with a toolchain or adjust the maven-compiler-plugin settings in the POM.

## Conventions and where to look in the code

- Core entry points: `org.seasar.dao.EntityManager`, `org.seasar.dao.SqlParser`.
- Metadata / mapping: packages and classes under `s2-dao/src/main/java/org/seasar/dao/` (DaoMetaData, BeanMetaData, RowCreator, PropertyTypeFactory, etc.).
- DB-specific hooks: `org.seasar.dao.dbms` package.
- Errors related to SQL files and parsing are defined as runtime exceptions in the same package (e.g., `SqlFileNotFoundRuntimeException`).

## Examples

See `s2-dao-examples` for usage examples. Those modules depend on `s2-dao` and show how to wire DAO interfaces and SQL files in an application.

## License

This project is licensed under the Apache License 2.0. See `Apache_Software_License_2.0.txt` for details.

## Contributing

Contributions are welcome. This repository contains legacy code (Java 1.4 era); if you propose modernizations (source/target update, CI changes), please document compatibility decisions and test on supported JDKs.

## Useful links

- Project website: http://s2dao.seasar.org/
- Issue tracker referenced in the POM: https://www.seasar.org/issues/browse/DAO

