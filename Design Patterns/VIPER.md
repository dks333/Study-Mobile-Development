# VIPER Design Pattern

! [VIPER] (/Swifty&#32;Notes/VIPER.png)



## Basics

### View

- User Interface where user interacts or see or input information
- Examples: UITableView, UICollectionView, UIView, UIButton, etc.

### Interactor

- Logic layer: get data from database and provide logical functions
- Examples: map data to another type, provide bonus when user finishes a task, etc.

### Presenter

- **View** asks **Presenter** for information/data. **Presenter** asks **Interactor** to return data
- **Presenter** communicates with **Router** to open new screens, but **Router** have the logic of transition

### Entity (Model)

### Routing

- Navigation logics

- Examples: ```pushViewController()```, ```addSubView()```, etc.

## Benefits

- Make your codes scalable, easier to test each layer
- Make your ViewController lightweight
- BUild the app based on use cases or behaviors

## Memory management

- **Router** keeps a weak reference of the **View** and the **Presenter**
- **Presener** hold strong refernces of **Router** and **Interactor**
- **Interactor** keeps a weak reference of **Presenter**
- **View** keeps a strong reference of **Presenter**

