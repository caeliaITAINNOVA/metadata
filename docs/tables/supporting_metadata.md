
<style>
  .md-typeset h1,
  .md-content__button {
    display: none;
  }
</style>
| Concept                     | Key         | Subkey | Type      | Example Value | Comment                                                  | Condition |
| --------------------------- | ----------- | ------ | --------- | ------------- | -------------------------------------------------------- | --------- |
| Person                      |             |        |           |               |                                                          |           |
|                             | ID          |        | ID / URI  |               | Unique identifier for the Person                         |           |
|                             | Created at  |        | ISO 8601  |               | Date of creation                                         |           |
|                             | Version     |        | Integer   |               | Version number of the Person                             |           |
|                             | First name  |        | Text      |               | First name of the Person                                 |           |
|                             | Last name   |        | Text      |               | Last name of the Person                                  |           |
|                             | Email       |        | Email     |               | Email address of the Person                              |           |
|                             | CV          |        | Text      |               | Short description of the Person                          |           |
|                             | Image       |        | Image     |               | Profile picture of the Person                            |           |
|                             | Affiliation |        | ID / URI  |               | Legal Entity the Person is affiliated with               |           |
| Legal Entity (Organization) |             |        |           |               |                                                          |           |
|                             | ID          |        | ID / URI  |               | Unique identifier for the Legal Entity                   |           |
|                             | Created at  |        | ISO 8601  |               | Date of creation                                         |           |
|                             | Version     |        | Integer   |               | Version number of the Legal Entity                       |           |
|                             | Author      |        | ID / URI  |               | Identifier of the Author of the Legal Entity             |           |
|                             | Name        |        | Text      |               | Name of the Legal Entity                                 |           |
|                             | Description |        | Text      |               | Description of the Legal Entity                          |           |
|                             | Logo        |        | Image     |               | Logo of the Legal Entity                                 |           |
|                             | URL         |        | URL       |               | Website of the Legal Entity                              |           |
|                             | Location    |        | ID / URI? |               | Physical address of the Legal Entity                     |           |
|                             | Phone       |        | String    |               | Phone Number of the Legal Entity                         |           |
|                             | VAT ID No.  |        | String    |               | VAT ID Number of the Legal Entity                        |           |
| IP Family                   |             |        |           |               |                                                          |           |
|                             | ID          |        | ID / URI  |               | Unique identifier for the IP Fam.                        |           |
|                             | Created at  |        | ISO 8601  |               | Date of creation                                         |           |
|                             | Version     |        | Integer   |               | Version number of the IP Family                          |           |
|                             | Author      |        | ID / URI  |               | Identifier of the Author of the IP Family                |           |
|                             | Manager     |        | ID / URI  |               | Identifier of the Legal Entity managing the IP Family    |           |
|                             | Name        |        | Text      |               | Technical Name of the IP Family                          |           |
|                             | Image       |        | Image     |               | Picture of the IP Family                                 |           |
|                             | Model No.   |        | Text      |               | Number defined by the IP Man.                            |           |
|                             | Description |        | Text      |               | Description of the IP Family                             |           |
|                             | Capacity    |        | Text      |               | Capacity of the IP Family                                |           |
|                             | IP Man.     |        | ID / URI  |               | Identifier of the IP Manufacturer (Legal Entity)         |           |
| IP Instance                 |             |        |           |               |                                                          |           |
|                             | ID          |        | ID / URI  |               | Unique identifier for the IP Inst.                       |           |
|                             | Created at  |        | ISO 8601  |               | Date of creation                                         |           |
|                             | Version     |        | Integer   |               | Version number of the IP Instance                        |           |
|                             | Author      |        | ID / URI  |               | Identifier of the Author of the IP Instance              |           |
|                             | Operator    |        | ID / URI  |               | Identifier of the Legal Entity operating the IP Instance |           |
|                             | IP Family   |        | ID / URI  |               | Reference to the IP Family                               |           |
|                             | Name        |        | Text      |               | Name of the IP Instance                                  |           |
|                             | Image       |        | Image     |               | Picture of the IP Instance                               |           |
|                             | Serial No.  |        | Text      |               | Number defined by the IP Man.                            |           |
|                             | Description |        | Text      |               | Description of the IP Instance                           |           |
|                             | Location    |        | ID / URI? |               | Physical location of the IP Instance                     |           |
