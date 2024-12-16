SQL
CREATE TABLE matches (
  id INT PRIMARY KEY AUTO_INCREMENT,
  homeTeam VARCHAR(255),
  awayTeam VARCHAR(255),
  kickOff DATETIME,
  league VARCHAR(255)
);
predictions.sql
SQL
CREATE TABLE predictions (
  id INT PRIMARY KEY AUTO_INCREMENT,
  matchId INT,
  prediction VARCHAR(255),
  probability FLOAT,
  FOREIGN KEY (matchId) REFERENCES matches(id)
);
