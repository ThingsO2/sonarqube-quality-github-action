# Sonar Action Quality Checked

The action retrieves the current analysis of the project and breaks the execution in case of Quality Gate Status is not Passsed.

## Action input parameters

| Parameter           | Description                                        | required | default |
| --------------------| :------------------------------------------------- | -------- | ------- |
| token               | SonarQube login token                              | yes      |         |
| url                 | SonarQube server url                               | yes      |         |

## Sample Configuration
```yml
  steps:
    - uses: thingso2/sonarqube-quality-github-action@<version>
      with:
        url: ${{ secrets.SONARQUBE_HOST }}
        token: ${{ secrets.SONARQUBE_TOKEN }}
```

## Technical decisions
At this moment, the process is using the information of the sonar scanner `./target/sonar/report-task.txt`` for obtain the analisys status form Sonar API. 