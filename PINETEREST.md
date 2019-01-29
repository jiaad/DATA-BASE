CREATE TABLE 'pins'(
  'id' INTEGER PRIMARY KEY AUTOINCREMENT,
  'image_pin' TEXT,
   'comm_id' INTEGER,
  FOREIGN KEY (comm_id) REFERENCES commentaires(id)
  );

CREATE TABLE 'commentaires'(
  'id' INTEGER PRIMARY KEY AUTOINCREMENT,
  'body' TEXT,
  'pins_id' INTEGER,
  FOREIGN KEY (pins_id) REFERENCES pins(id) 
);
SELECT * FROM commentaires;

INSERT INTO pins(image_pin) VALUES('wewewe');
INSERT INTO commentaires(body , pins_id) VALUES("comm mon gars" , 1);
SELECT * FROM commentaires;