Tu dois créer une plateforme d'apprentissage en ligne. Il y a plein de cours. Chaque cours a un titre et une description. Enfin, chaque cours a plusieurs leçons, qui ont un titre et un body.


CREATE TABLE 'cours'(
  'id' INTEGER PRIMARY KEY AUTOINCREMENT,
  'titre' TEXT,
  'description' TEXT
);
CREATE TABLE 'lecons'(
  'id' INTEGER PRIMARY KEY AUTOINCREMENT,
  'titre' TEXT,
  'body' TEXT,
  'cours_id' INTEGER,
  FOREIGN KEY(cours_id) REFERENCES cours(id) );

SELECT * FROM lecons;
SELECT * FROM cours;


INSERT INTO cours(titre,description) VALUES('js','nul a iech');
INSERT INTO lecons(titre, body, cours_id) VALUES('syntaxes', 'mange bien', 1);
SELECT * FROM lecons;