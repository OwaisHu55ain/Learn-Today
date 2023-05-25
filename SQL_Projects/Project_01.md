# SQL Project

Main areas of focus
1. Orders
2. Stock Control
3.  Staff

**Orders Data Required:**
1. Item Name
2. Item Price
3. Quantity
4. Customer Name
5. Delivery Address

**Open _Quick-Database-Diagram_**

**Tables Schema:**
```
CREATE TABLE `Orders` (
    `Row_ID` INT  NOT NULL ,
    `Order_ID` VARCHAR(10)  NOT NULL ,
    `Created_at` DATETIME  NOT NULL ,
    `Item_ID` VARCHAR(10)  NOT NULL ,
    `Quantity` INT  NOT NULL ,
    `Customer_ID` INT  NOT NULL ,
    `Delivery` BOOLEAN  NOT NULL ,
    `Address_ID` INT  NOT NULL ,
    PRIMARY KEY (
        `Row_ID`
    )
);

CREATE TABLE `Customers` (
    `Customer_ID` INT  NOT NULL ,
    `Cust_FirstName` VARCHAR(50)  NOT NULL ,
    `Cust_LastName` VARCHAR(50)  NOT NULL ,
    PRIMARY KEY (
        `Customer_ID`
    )
);

CREATE TABLE `Address` (
    `Address_ID` INT  NOT NULL ,
    `Delivery_Address1` VARCHAR(200)  NOT NULL ,
    `Delivery_Address2` VARCHAR(200)  NULL ,
    `Delivery_City` VARCHAR(50)  NOT NULL ,
    `Delivery_ZipCode` VARCHAR(20)  NOT NULL ,
    PRIMARY KEY (
        `Address_ID`
    )
);

CREATE TABLE `Items` (
    `Item_ID` VARCHAR(10)  NOT NULL ,
    `SKU` VARCHAR(20)  NOT NULL ,
    `Item_Name` VARCHAR(200)  NOT NULL ,
    `Item_Cat` VARCHAR(200)  NOT NULL ,
    `Item_Size` VARCHAR(10)  NOT NULL ,
    `Item_Price` DECIMAL(10,2)  NOT NULL ,
    PRIMARY KEY (
        `Item_ID`
    )
);

CREATE TABLE `Ingredients` (
    `Ing_ID` INT  NOT NULL ,
    `Ing_Name` VARCHAR(200)  NOT NULL ,
    `Ing_Weight` INT  NOT NULL ,
    `Ing_Meas` VARCHAR(20)  NOT NULL ,
    `Ing_Price` DECIMAL(5,2)  NOT NULL ,
    PRIMARY KEY (
        `Ing_ID`
    )
);

CREATE TABLE `Recipe` (
    `Row_ID` INT  NOT NULL ,
    `Recipe_ID` VARCHAR(20)  NOT NULL ,
    `Ing_ID` VARCHAR(10)  NOT NULL ,
    `Quantiry` INT  NOT NULL ,
    PRIMARY KEY (
        `Row_ID`
    )
);

CREATE TABLE `Inventory` (
    `Inv_ID` INT  NOT NULL ,
    `Item_ID` VARCHAR(10)  NOT NULL ,
    `Quantity` INT  NOT NULL ,
    PRIMARY KEY (
        `Inv_ID`
    )
);

CREATE TABLE `Staff` (
    `Staff_ID` VARCHAR(20)  NOT NULL ,
    `First_Name` VARCHAR(50)  NOT NULL ,
    `Last_Name` VARCHAR(50)  NOT NULL ,
    `Position` VARCHAR(100)  NOT NULL ,
    `Hourly_Rate` DECIMAL(5,2)  NOT NULL ,
    PRIMARY KEY (
        `Staff_ID`
    )
);

CREATE TABLE `Rota` (
    `Row_ID` INT  NOT NULL ,
    `Rota_ID` VARCHAR(20)  NOT NULL ,
    `Date` DATETIME  NOT NULL ,
    `Shift_ID` VARCHAR(20)  NOT NULL ,
    `Staff_ID` VARCHAR(20)  NOT NULL ,
    PRIMARY KEY (
        `Row_ID`
    )
);

CREATE TABLE `Shift` (
    `Shift_ID` VARCHAR(20)  NOT NULL ,
    `Day_of_Week` VARCHAR(10)  NOT NULL ,
    `Start_Time` TIME  NOT NULL ,
    `End_Time` TIME  NOT NULL ,
    PRIMARY KEY (
        `Shift_ID`
    )
);

ALTER TABLE `Customers` ADD CONSTRAINT `fk_Customers_Customer_ID` FOREIGN KEY(`Customer_ID`)
REFERENCES `Orders` (`Customer_ID`);

ALTER TABLE `Address` ADD CONSTRAINT `fk_Address_Address_ID` FOREIGN KEY(`Address_ID`)
REFERENCES `Orders` (`Address_ID`);

ALTER TABLE `Items` ADD CONSTRAINT `fk_Items_Item_ID` FOREIGN KEY(`Item_ID`)
REFERENCES `Orders` (`Item_ID`);

ALTER TABLE `Ingredients` ADD CONSTRAINT `fk_Ingredients_Ing_Name` FOREIGN KEY(`Ing_Name`)
REFERENCES `Recipe` (`Ing_ID`);

ALTER TABLE `Recipe` ADD CONSTRAINT `fk_Recipe_Row_ID` FOREIGN KEY(`Row_ID`)
REFERENCES `Items` (`SKU`);

ALTER TABLE `Inventory` ADD CONSTRAINT `fk_Inventory_Item_ID` FOREIGN KEY(`Item_ID`)
REFERENCES `Recipe` (`Ing_ID`);

ALTER TABLE `Staff` ADD CONSTRAINT `fk_Staff_Staff_ID` FOREIGN KEY(`Staff_ID`)
REFERENCES `Rota` (`Staff_ID`);

ALTER TABLE `Rota` ADD CONSTRAINT `fk_Rota_Date` FOREIGN KEY(`Date`)
REFERENCES `Orders` (`Created_at`);

ALTER TABLE `Shift` ADD CONSTRAINT `fk_Shift_Shift_ID` FOREIGN KEY(`Shift_ID`)
REFERENCES `Rota` (`Shift_ID`);
```
