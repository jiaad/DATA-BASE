CREATE TABLE 'users'(
id INTEGER PRIMARY KEY AUTOINCREMENT,
'news_title' TEXT
);
INSERT INTO users(news_title) VALUES ('va te faire foutre');

CREATE TABLE 'commentaires'(
id INTEGER PRIMARY KEY AUTOINCREMENT,
'comments' TEXT,
user_id_post INTEGER,
FOREIGN KEY (user_id_post) REFERENCES users(id)
);

CREATE TABLE 'reply_commentaires'(
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    rpl_comm TEXT,
    comm_id_orgnl INTEGER,
    user_post_id INTEGER,
    FOREIGN KEY (comm_id_orgnl) REFERENCES commentaires(id)
    FOREIGN KEY (user_post_id) REFERENCES users(id)
);

INSERT INTO commentaires(comments , user_id_post) VALUES('commentaires de merde', 1);
INSERT INTO reply_commentaires(rpl_comm , comm_id_orgnl, user_post_id) VALUES('ceci est un reply', 1, 1);

SELECT * FROM users;
SELECT * FROM commentaires;
SELECT * FROM reply_commentaires;