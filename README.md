# Indonesian Administrative Regions Database

This repository contains SQL database structure for Indonesian administrative regions, including provinces, cities, districts, subdistricts, and postal codes.

## Database Structure

The database consists of 5 main tables:

### 1. Provinces (`provinces`)
- `id` - Primary key
- `province_name` - Name of the province

### 2. Cities (`cities`)
- `id` - Primary key
- `city_name` - Name of the city
- `province_id` - Foreign key referencing provinces table

### 3. Districts (`districts`)
- `id` - Primary key
- `district_name` - Name of the district
- `city_id` - Foreign key referencing cities table

### 4. Subdistricts (`subdistricts`)
- `id` - Primary key
- `subdistrict_name` - Name of the subdistrict
- `district_id` - Foreign key referencing districts table

### 5. Zip Codes (`zip_codes`)
- `id` - Primary key
- `subdistrict_id` - Foreign key referencing subdistricts table
- `code` - Postal code number

## Database Relationships
```
provinces -> cities -> districts -> subdistricts -> zip_codes
```

## Technical Details
- Database Engine: MyISAM
- Character Set: latin1
- Collation: latin1_swedish_ci

## Usage
1. Import the SQL file into your MySQL database
2. Use the relationships between tables to query location data
3. Can be used for:
   - Address forms
   - Location-based services
   - Geographic data analysis
   - Postal code validation

## Contributing
Feel free to contribute by:
1. Creating issues for bugs or improvements
2. Submitting pull requests with data updates
   
Note: Please ensure to maintain data integrity when using or modifying the database structure.
