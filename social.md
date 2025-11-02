# table : USER ONE TO MANY CON I POST

- id UNIQUE/AUTO INCREMENT BIGINT,
- last_name NOT NULL VARCHAR(50),
- name NOT NULL VARCHAR(50),
- email NOT NULL UNIQUE VARCHAR(100),
- date_of_birth NOT NULL DATE,
- password NOT NULL VARCHAR(100),
- username NULL VARCHAR(50)

## table : POST ONE TO MANY CON I MEDIA

- id UNIQUE/AUTO INCREMENT BIGINT,
- utente_id FOREIGN KEY NOT NULL BIGINT,
- data e ora post TIMESTAMP NOT NULL,
- titolo post VARCHAR(50) NULL,
- descrizione post TEXT NULL ,
- contenuto post NOT NULL TEXT

### pivot table : LIKE MANY TO MANY CON I POST E UTENTE

- id UNIQUE/AUTO INCREMENT BIGINT,
- utente_id FOREIGN KEY NOT NULL BIGINT,
- post_id FOREIGN KEY NOT NULL BIGINT,
- UNIQUE(utente_id, post_id)

#### table : MEDIA --> MANY TO ONE COLLEGATA CON GLI ID ALL'UTENTE E ALL'ID DEI POST (tanti media collegati ad un utente e ad un post)

- id UNIQUE AUTO INCREMENT,
- nome file NOT NULL VARCHAR(50),
- tipo file NOT NULL VARCHAR(30) ('jpg' 'png' 'mp4'),
- URL VARCHAR (500) NOT NULL,
- utente_id FOREIGN KEY NOT NULL BIGINT,
- post_id FOREIGN KEY NOT NULL BIGINT
