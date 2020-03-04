# Préparation Visite Exlibris

## Nz Topology

### User management

Every user can use any libraries regardless of his university. In all librairies he has the same rights that would be available in his institution. Users are loaded in the NZ via SIS Loader. User\_group, Campus\_code, Job\_category were defined at the SIS level. This fields values are shared by all institutions 

#### CASE : 00622866

External users were loaded in NZ institution and copied in institution when their barcode were scanned at the circulation desk or when they signed in Primo. Problem. A User from 33PUDB\_UBM institution see a book from 33PUDB\_BXSA via 33PUDB\_UBM primo view. This user sign in but he can place a demand on the record because his account is not copied in 33PUDB\_BXSA. 

The patch sf:00622866 supposed to solve this issue but the issue is still there. 

{% embed url="https://www.loom.com/share/c4d908dc5d7b4fd497e6a10b546bbfa8" %}

#### Block and information sharing

When a user have a block on an institution the system should replicate this block to all institutions. In other term we want consortial blocks. In more, when an institution modify an external account this change should be impact NZ account and be shared between all institutions.

#### Register a New External User \(00742328\)

When a user does not yet have SIS account we use quick registration to create an external account.  This external accoubt will not be toattly synchronise with SIS bexause User\_group, Campus\_code and Job\_category will not be changed by SIS Loader.

### Records management

Any record created in system was created in Network Zone. \(central\_record\_management = ENFORCE\_NETWORK\)

#### Records suppression for discovery \(case 00621579\)

The parameter "suppressBibWithSuppressedHol" is not relevant in Network topology. When an isnstitution supress from discovery the last holding linked to a record. The record is still published in Primo however there don't have any inventory in an other institution.

#### Records delation 

When a staff user delete a record by deleting the last linked inventory \(holding or portfolio\). This record is still active in NZ without inventory.





   



