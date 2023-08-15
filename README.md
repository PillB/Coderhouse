# Coderhouse

```mermaid
    Species ||--o{ CoffeeData : "FK_SpeciesID";
    Species {
        int SpeciesID PK
        string Species
    };

    Owner ||--o{ CoffeeData : "FK_OwnerID";
    Owner {
        int OwnerID PK
        string Owner
        string Certification.Address
        string Certification.Contact
    };

    Country ||--o{ CoffeeData : "FK_CountryID";
    Country {
        int CountryID PK
        string Country.of.Origin
    };

    Farm ||--o{ CoffeeData : "FK_FarmID";
    Farm {
        int FarmID PK
        string Farm.Name
        string Altitude
        string Region
        float altitude_low_meters
        float altitude_high_meters
        float altitude_mean_meters
    };

    Company ||--o{ CoffeeData : "FK_CompanyID";
    Company {
        int CompanyID PK
        string Company
        string ICO.Number
    };

    Processing ||--o{ CoffeeData : "FK_ProcessingID";
    Processing {
        int ProcessingID PK
        string Processing.Method
    };

    Certification ||--o{ CoffeeData : "FK_CertificationID";
    Certification {
        int CertificationID PK
        string Certification.Body
    };

    Color ||--o{ CoffeeData : "FK_ColorID";
    Color {
        int ColorID PK
        string Color
    };

    CoffeeData {
        int CoffeeID PK
        int SpeciesID FK
        int OwnerID FK
        int CountryID FK
        int FarmID FK
        int CompanyID FK
        int ProcessingID FK
        int CertificationID FK
        int ColorID FK
        string Aroma
        string Flavor
        string Aftertaste
        string Acidity
        string Body
        string Balance
        string Uniformity
        string Clean.Cup
        string Sweetness
        float Cupper.Points
        float Total.Cup.Points
        float Moisture
        int Category.One.Defects
        int Quakers
        int Category.Two.Defects
        date Expiration
    };
```
