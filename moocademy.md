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