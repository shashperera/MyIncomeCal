# MyIncomeCal
Spring Boot + PostgreSQL income calculator project using Ansible

1. Install Ansible and required collection:
    sudo apt update
    sudo apt install ansible
    ansible-galaxy collection install community.postgresql


2. Create your Ansible playbook (playbook.yml): This playbook installs Java, Maven, PostgreSQL, and sets up the database and user.
3. Run the playbook:
    ansible-playbook playbook.yml

4. Update your Spring Boot application.properties:
    spring.datasource.url=jdbc:postgresql://localhost:5432/income_db
    spring.datasource.username=income_user
    spring.datasource.password=income_pass
    spring.jpa.hibernate.ddl-auto=update
    spring.jpa.show-sql=true

5. Build and run your Java project:
    mvn clean install
    mvn spring-boot:run

