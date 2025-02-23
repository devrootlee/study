###### AWS

<details>
<summary>EC2</summary>


- 스프링부트 프로젝트 ec2서버에서 실행시키기(Amazon Linux 2)s
1. pem key 권한 설정
````
chmod 400 [/path/to/your-key].pem  # 키 파일의 권한 설정
````
2. ec2 public ip 주소를 얻은 뒤 ssh로 접근 
````
ssh -i [/path/to/your-key].pem ec2-user@[EC2 퍼블릭 IP]
````

3. ssh로 ec2 서버에 파일 옮기기(옮기는 폴더가 있어야함!)
````
scp -i [/path/to/your-key].pem [/path/to/your-application.jar] ec2-user@[your-ec2-public-ip]:/home/ec2-user/
````
4. Spring boot project 실행
````
java -jar [/path/to/your-application.jar]
````
5. Spring boot project 멈춤
````
Ctrl + C
````
</details>

<details>
<summary>S3</summary>
  접히는 내용입니다.  
  여러 줄의 텍스트나 코드 블록도 넣을 수 있습니다.
</details>

<details>
<summary>RDS</summary>
  접히는 내용입니다.  
  여러 줄의 텍스트나 코드 블록도 넣을 수 있습니다.
</details>
