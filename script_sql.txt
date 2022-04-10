create table dim_product(
  product_id integer primary key,
  productline varchar(75)
  );
  
  select * from dim_product;
  
  
  create table dim_geografia(
  geografia_id integer primary key,
  country varchar(75),
  city varchar(75),
  state varchar(75),
  territory varchar(75)
  );
  
  select * from dim_product;
  
  
  create table dim_dealer(
  dealer_id integer primary key,
  dealsize varchar(75)
  );
 
   select * from dim_dealer;
   
   create table dim_customer(
     customer_id integer primary key,
     customername varchar(100),
     phone varchar(75),
     contactfirstname varchar(75),
     contactlastname varchar(75)
    );
    
select *
from dim_customer;

create table dim_tiempo(
  tiempo_id integer primary key,
  orderdate varchar(75),
  qtr_id integer,
  month_id integer,
  year_id integer
  );
  
  select *
  from dim_tiempo
  
  create table fact_table(
    sales_id integer primary key,
    customer_id integer,
    product_id integer,
    geografia_id integer,
    tiempo_id integer,
    dealer_id integer,
    ordernumber integer,
    quantityordered integer,
    orderlinenumber integer,
    sales integer
    );
    
    
ALTER TABLE fact_table
ADD FOREIGN KEY (customer_id)references dim_customer(customer_id);

ALTER TABLE fact_table
ADD FOREIGN KEY (product_id) REFERENCES dim_product(product_id);

ALTER TABLE fact_table
ADD FOREIGN KEY (geografia_id) REFERENCES dim_geografia(geografia_id);

ALTER TABLE fact_table
ADD FOREIGN KEY (tiempo_id) REFERENCES dim_tiempo(tiempo_id);

ALTER TABLE fact_table
ADD FOREIGN KEY (dealer_id) REFERENCES dim_dealer(dealer_id);


select *
from fact_table