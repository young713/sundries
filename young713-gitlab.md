```
web:
  image: 'gitlab/gitlab-ce:latest'
  restart: always
  hostname: 'gitlab.young713.refinedev.io'
  container_name: gitlab
  environment:
    GITLAB_OMNIBUS_CONFIG: |
            external_url 'http://gitlab.young713.refinedev.io'
            registry_external_url 'http://gitlab.young713.refinedev.io:5005'
      # Add any other gitlab.rb configuration here, each on its own line
  ports:
    - '80:80'
    - '443:443'
    - '823:22'
    - '5005:5005'
  volumes:
    - '/home/young713/gitlab/config:/etc/gitlab'
    - '/home/young713/gitlab/logs:/var/log/gitlab'
    - '/home/young713/gitlab/data:/var/opt/gitlab'
    - '/home/young713/gitlab/backups:/var/opt/gitlab/backups' # 백업 폴더 추가
```
