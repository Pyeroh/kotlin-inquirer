<h1 align="center">
    <a href="https://kotlin-inquirer.github.io/kotlin-inquirer/">
        <img src="https://raw.githubusercontent.com/kotlin-inquirer/kotlin-inquirer/master/assets/kotlin-inquirer-logo.png" width="40%"/>
    </a>
</h1>

[![Build Status](https://travis-ci.com/kotlin-inquirer/kotlin-inquirer.svg?branch=master)](https://travis-ci.org/kotlin-inquirer/kotlin-inquirer)
[![Apache License V.2](https://img.shields.io/badge/license-Apache%20V.2-blue.svg)](https://github.com/kotlin-inquirer/kotlin-inquirer/blob/master/LICENSE) 
[![](https://jitpack.io/v/kotlin-inquirer/kotlin-inquirer.svg)](https://jitpack.io/#kotlin-inquirer/kotlin-inquirer)

> A collection of common interactive command line user interfaces written in [![Pure Kotlin](https://img.shields.io/badge/100%25-kotlin-blue.svg)](https://kotlinlang.org/) inspired by [Inquirer.js](https://github.com/SBoudrias/Inquirer.js "Inquirer.js") 

<p align="center">
  <img src="https://raw.githubusercontent.com/kotlin-inquirer/kotlin-inquirer/new_gifs/assets/pizza.gif?raw=true" width="80%"/>
</p>

## :rocket: Run Demo Using [kscript](https://github.com/holgerbrandl/kscript "kscript")
Remote scriplet [raw-URL](https://raw.githubusercontent.com/kotlin-inquirer/kotlin-inquirer/master/scripts/src/pizza.kts 
"pizza.kts") 


```
kscript https://git.io/fjj2P
```

Or clone it

```
git clone https://github.com/kotlin-inquirer/kotlin-inquirer.git
cd kotlin-inquirer
kscript ./scripts/src/pizza.kts
```


## :cloud: Download

### Gradle
```groovy
allprojects {
  repositories {
    maven { url 'https://jitpack.io' }
  }
}
```

```groovy
dependencies {
  implementation 'com.github.kotlin-inquirer:kotlin-inquirer:v0.0.2-alpha'
}
```

## :clipboard: Usages

#### Confirm

```kotlin
val isDelivery: Boolean = KInquirer.promptConfirm(message = "Is this for delivery?", default = false)
println("Is Delivery: $isDelivery")
```
<p align="center">
  <img src="https://raw.githubusercontent.com/kotlin-inquirer/kotlin-inquirer/new_gifs/assets/confirm.gif?raw=true" width="80%"/>
</p>

------

#### Input
```kotlin
val comments: String = KInquirer.promptInput(message = "Any comments on your purchase experience?")
println("Comments: $comments")
```
<p align="center">
  <img src="https://raw.githubusercontent.com/kotlin-inquirer/kotlin-inquirer/new_gifs/assets/input.gif?raw=true" width="80%"/>
</p>

------

#### Input Numbers
```kotlin
val quantity: BigDecimal = KInquirer.promptInputNumber(message = "How many do you need?")
println("Quantity: $quantity")
```
<p align="center">
  <img src="https://raw.githubusercontent.com/kotlin-inquirer/kotlin-inquirer/new_gifs/assets/input_numbers.gif?raw=true" width="80%"/>
</p>

------

#### Input Password
```kotlin
val password: String = KInquirer.promptInputPassword(message = "Enter Your Password:", hint = "password")
println("Password: $password")
```
<p align="center">
  <img src="https://raw.githubusercontent.com/kotlin-inquirer/kotlin-inquirer/new_gifs/assets/input_password.gif?raw=true" width="80%"/>
</p>


------

#### List
```kotlin
val size: String = KInquirer.promptList(message = "What size do you need?", choices = listOf("Large", "Medium", "Small"))
println("Size: $size")
```
<p align="center">
  <img src="https://raw.githubusercontent.com/kotlin-inquirer/kotlin-inquirer/new_gifs/assets/list.gif?raw=true" width="80%"/>
</p>

------

#### Checkbox
```kotlin
val toppings: List<String> = KInquirer.promptCheckbox(
    message = "What about the toppings?",
    choices = listOf(
        "Pepperoni and cheese",
        "All dressed",
        "Hawaiian",
    ),
)
println("Toppings: $toppings")
```
<p align="center">
  <img src="https://raw.githubusercontent.com/kotlin-inquirer/kotlin-inquirer/new_gifs/assets/checkbox.gif?raw=true" width="80%"/>
</p>

------

### :crystal_ball: Roadmap
#### Components
- [x] Confirm
- [x] Input
- [x] Input Numbers
- [x] Input Password
- [x] List
- [x] Checkbox
- [x] Input validation error message
- [x] Support Hint
- [x] Better package name

#### Operation
- [x] Examples
- [x] Travis-CI
- [x] Logo
- [ ] GIFs
- [ ] Maven Central
- [ ] codecov 


