CREATE TABLE Farmacia 
( 
    idFarmacia INT PRIMARY KEY,  
    nome_farmacia VARCHAR(255),  
    end_farmacia VARCHAR(255),  
    CNPJ_farmacia VARCHAR(20),  
    tel_farmacia VARCHAR(15)  
); 

CREATE TABLE Produto 
( 
    cod_produto INT PRIMARY KEY,  
    qtd_produto INT,  
    valor_produto DECIMAL(10, 2),  
    idFarmacia INT,  
    FOREIGN KEY (idFarmacia) REFERENCES Farmacia (idFarmacia)  
); 

CREATE TABLE Farmaceutico 
( 
    nome_farmaceutico VARCHAR(255),  
    RG_farmaceutico VARCHAR(20) PRIMARY KEY,  
    idFarmacia INT,  
    FOREIGN KEY (idFarmacia) REFERENCES Farmacia (idFarmacia)  
);
