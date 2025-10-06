# Habi Heritage System Class Diagram

This class diagram represents the backend domain models of the Habi Heritage system, showing their attributes and relationships.

```mermaid
classDiagram
    class User {
        +name: string
        +email: string
        +password: string
        +role: string
        +donations(): hasMany
        +checkouts(): hasMany
    }

    class Product {
        +name: string
        +description: string
        +price: float
        +image: string
        +checkouts(): hasMany
    }

    class Checkout {
        +user_id: int
        +items: json
        +total: float
        +user(): belongsTo
        +product(): belongsTo
    }

    class Donation {
        +user_id: int
        +amount: float
        +user(): belongsTo
    }

    class Fundraising {
        +title: string
        +description: string
    }

    class Gallery {
        +image: string
    }

    class HomeContent {
        +main_title: string
        +subtitle: string
        +highlight1_title: string
        +highlight1_desc: string
        +highlight2_title: string
        +highlight2_desc: string
        +highlight3_title: string
        +highlight3_desc: string
    }

    class Storytelling {
        +title: string
        +content: string
        +image: string
        +link: string
        +author: string
        +video: string
        +type: string
    }

    class Shortfilm {
        +title: string
        +video: string
    }

    class AdminMiddleware {
        +handle(Request, Closure): Response
    }

    User o-- Donation : has many
    User o-- Checkout : has many
    Product o-- Checkout : has many
    Checkout -- User : belongs to
    Checkout -- Product : belongs to
    Donation -- User : belongs to
    AdminMiddleware ..> User : checks role
    AdminMiddleware ..> Fundraising : manages
    AdminMiddleware ..> Gallery : manages
    AdminMiddleware ..> HomeContent : manages
    AdminMiddleware ..> Storytelling : manages
    AdminMiddleware ..> Shortfilm : manages
```

## Notes
- Attributes are based on the fillable arrays in the Eloquent models.
- Relationships are defined using Laravel's Eloquent relationships.
- User has a role field that can be 'user' or 'admin' for access control.
- AdminMiddleware checks the user's role for admin-only features.
- This diagram focuses on the backend models; controllers and frontend components are not included for simplicity.