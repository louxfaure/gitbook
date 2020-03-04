# Préparation Visite Exlibris

## Nz Topology

### User management

Every user can use any libraries regardless of his university. In all librairies the user has the same rights that would be available in his institution. Users are loaded in the NZ via SIS Loader. User\_group, Campus\_code, Job\_category were defined at the SIS level. This fields values are shared by all institutions 

#### CASE : 00622866

External users were loaded in NZ institution and copied in institution when their barcode were scanned at the circulation desk or when they signed in on Primo for the first time. Problem. A User from 33PUDB\_UBM institution see a book from 33PUDB\_BXSA via 33PUDB\_UBM primo view. This user signed in but he couldn't place a demand on the record because his account is not copied in 33PUDB\_BXSA. 

The patch sf:00622866 was supposed to solve this issue but the issue is still here. 

{% embed url="https://www.loom.com/share/c4d908dc5d7b4fd497e6a10b546bbfa8" %}

#### Block and information sharing

When a user has a block on an institution the system should replicate this block to all institutions. In other term we want consortial blocks. Furthermore, when an institution modify an external account this change should be replicated on NZ account and shared between all institutions.

#### Register a New External User \(00742328\)

When a user does not yet have SIS account we use quick registration to create an external account.  This external account will not be totally synchronised with SIS because User\_group, Campus\_code and Job\_category are unmodifiable by SIS Loader.

### Records management

Any record created in system was created in Network Zone. \(central\_record\_management = ENFORCE\_NETWORK\)

#### Records suppression for discovery \(case 00621579\)

The parameter "suppressBibWithSuppressedHol" is not relevant in Network topology. When an institution supress from discovery the last holding linked to a record in all institutions, that record is still published in Primo eventhought there is no more inventory.

#### Records deletion 

When a staff user deletes a record by deleting the last linked inventory \(holding or portfolio\), this record is still active in NZ even without inventory.





   



