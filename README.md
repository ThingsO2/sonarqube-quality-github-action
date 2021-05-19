# Sonar Action Quality Checked

The action retrieves the current analysis of the project and breaks the execution in case of Quality Gate Status is not
Passsed.

## Action input parameters

| Parameter           | Description                                        | required | default |
| --------------------| :------------------------------------------------- | -------- | ------- |
| token               | SonarQube login token                              | yes      |         |
| url                 | SonarQube server url                               | yes      |         |
| report-path         | Generated Report txt path                          | false    | ./target/sonar/report-task.txt |

## Sample Configuration

```yml
  steps:
    - uses: thingso2/sonarqube-quality-github-action@<version>
      with:
        url: ${{ secrets.SONARQUBE_HOST }}
        token: ${{ secrets.SONARQUBE_TOKEN }}
```