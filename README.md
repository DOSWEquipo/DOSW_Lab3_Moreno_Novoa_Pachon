# DOSW Lab 3 - Moreno, Novoa & Pachón

Repository dedicated to **user research, requirements gathering, and UI/UX design**. It integrates specification techniques such as context diagrams, requirements definition and analysis, mockups, and navigation flows.

---

## Maven Project Structure

The basic project structure was created using the `maven-archetype-quickstart` archetype with the following command:

```bash
mvn archetype:generate -DgroupId=edu.eci.dosw.lab -DartifactId=DOSW-Laboratorio3 -DarchetypeArtifactId=maven-archetype-quickstart -DinteractiveMode=false
```

This command generates a basic Maven project with the standard directory structure and configuration files required for a Java project.

---

## Maven and GitHub Questions

### 1. What is a Maven archetype?

A Maven archetype is a template used to quickly create the basic structure of a project. It provides a predefined structure of directories and files that can be used as a starting point for developing a project.

### 2. What is the purpose of the `maven-archetype-quickstart` archetype?

The purpose of the `maven-archetype-quickstart` archetype is to quickly create a basic Java Maven project. It generates an initial project structure that includes a `pom.xml` file, a main Java class, and a test class.

### 3. What command can be used to create a project based on a Maven archetype?

The command used to create a project based on a Maven archetype is:

```bash
mvn archetype:generate
```

This command invokes the **Maven Archetype Plugin** and allows a new project to be generated from an existing archetype. It uses information provided by the developer, such as the project name, `groupId`, `artifactId`, and the archetype to be used. Maven then generates the directory structure and files defined by the selected archetype.

### 4. What is a Pull Request in GitHub?

A Pull Request (PR) in GitHub is a request to merge changes from one branch into another branch of a repository. It allows collaborators to review the changes, leave comments, and suggest modifications before the changes are merged.

### 5. How do you create a Pull Request in GitHub?

To create a Pull Request in GitHub:

1. Make the changes in a branch different from the main branch.
2. Commit the changes.
3. Push the branch to the remote repository.
4. Open the repository on GitHub.
5. Select **Pull requests**.
6. Click **New pull request**.
7. Select the branch containing the changes and the target branch.
8. Add a title and description for the Pull Request.
9. Click **Create pull request**.

### 6. How do you approve a Pull Request in GitHub?

To approve a Pull Request:

1. Open the Pull Request on GitHub.
2. Review the changes and the code.
3. Click **Review changes**.
4. Select **Approve**.
5. Add an optional comment.
6. Click **Submit review**.

After the Pull Request has been approved and the repository requirements have been met, a user with the necessary permissions can merge it into the target branch.

### 7. References

* Apache Maven. (n.d.). *Maven Archetype Plugin*. Apache Maven. https://maven.apache.org/archetype/maven-archetype-plugin/

* Apache Maven. (n.d.). *Maven Getting Started Guide*. Apache Maven. https://maven.apache.org/guides/getting-started/

* GitHub Docs. (n.d.). *About pull requests*. GitHub. https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests

