# USER_TABLE
user table in mysql


## TableCode:
```mysql
CREATE TABLE users (
    id INT PRIMARY KEY AUTO_INCREMENT,
    username VARCHAR(255) NOT NULL,
    email VARCHAR(255) NOT NULL,
    phonenumber VARCHAR(15),
    birthdate DATE,
    password VARCHAR(255) NOT NULL,
    last_login_ip VARCHAR(45),
    last_login_date TIMESTAMP,
    last_login_loc VARCHAR(255),
    joined_date TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
    is_use_referance BOOLEAN,
    use_to_join_referance VARCHAR(255),
    referance_code VARCHAR(255)
);
```

## View:
| Alan                 | Tür                  | Açıklama                                      |
|----------------------|----------------------|-----------------------------------------------|
| id                   | INT                  | Kullanıcıların benzersiz tanımlayıcısı        |
| username             | VARCHAR(255)         | Kullanıcı adı                                 |
| email                | VARCHAR(255)         | Kullanıcı e-posta adresi                      |
| phonenumber          | VARCHAR(15)          | Telefon numarası                              |
| birthdate            | DATE                 | Doğum tarihi                                  |
| password             | VARCHAR(255)         | Kullanıcı şifresi                             |
| last_login_ip        | VARCHAR(45)          | Son girişte kullanılan IP adresi              |
| last_login_date      | TIMESTAMP            | Son giriş tarihi ve saati                    |
| last_login_loc       | VARCHAR(255)         | Son girişin yapıldığı konum                   |
| joined_date          | TIMESTAMP DEFAULT CURRENT_TIMESTAMP | Kullanıcının kaydolduğu tarih ve saat (varsayılan olarak şu anki tarih ve saat) |
| is_use_referance     | BOOLEAN              | Referans kullanılıyor mu? (boolean)          |
| use_to_join_referance| VARCHAR(255)         | Referans kullanılarak katılım (join) için kullanılan değer |
| referance_code       | VARCHAR(255)         | Referans kodu                                 |
