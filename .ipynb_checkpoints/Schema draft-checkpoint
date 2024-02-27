CREATE TABLE contacts(
	contact_id INT PRIMARY KEY,
	first_name VARCHAR,
  last_name VARCHAR,
  email VARCHAR
);

CREATE TABLE category(
	category_ids VARCHAR PRIMARY KEY,
	category VARCHAR
);

CREATE TABLE subcategory(
	subcategory_ids VARCHAR PRIMARY KEY,
	subcategory VARCHAR
);

CREATE TABLE campaign(
  cf_id INT,
  contact_id INT,
  company_name VARCHAR,
  description TEXT,
  goal DECIMAL,
  pledged DECIMAL,
  outcome VARCHAR,
  backers_count int,
  country VARCHAR,
  currency VARCHAR,
  launch_date DATE,
  end_date DATE,
  category VARCHAR,
  subcategory VARCHAR,
  category_id VARCHAR,
  subcategory_id VARCHAR,
  PRIMARY KEY (cf_id),
  FOREIGN KEY (contact_id) REFERENCES contacts(contact_id),
  FOREIGN KEY (category_id) REFERENCES category(category_ids),
  FOREIGN KEY (subcategory_id) REFERENCES subcategory(subcategory_ids)
);
