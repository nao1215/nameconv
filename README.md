[![UnitTest](https://github.com/nao1215/nameconv/actions/workflows/unit_test.yml/badge.svg)](https://github.com/nao1215/nameconv/actions/workflows/unit_test.yml)
[![reviewdog](https://github.com/nao1215/nameconv/actions/workflows/review_dog.yml/badge.svg)](https://github.com/nao1215/nameconv/actions/workflows/review_dog.yml)
[![codecov](https://codecov.io/gh/nao1215/nameconv/branch/main/graph/badge.svg?token=DO641K2SOW)](https://codecov.io/gh/nao1215/nameconv)
[![Go Report Card](https://goreportcard.com/badge/github.com/nao1215/nameconv)](https://goreportcard.com/report/github.com/nao1215/nameconv)

# nameconv
**nameconv** is library that converts string naming conventions. 
    
## Convert functions
The following function converts the string passed as an argument to the specified naming convention.
| function|description|
|:--|:--|
|ToSnakeCase()| convert string to snake_case style |
|ToChainCase()| convert string to chain-case style|
|ToKebabCase()| same as ToChainCase()|
|ToCamelCase()| convert string to camelCase style|
|ToPascalCase()| convert string to PascalCase style|
|ToFlatCase()| convert string to flatcase style|
|ToUpperCase()| convert string to UPPER_CASE style|  
    
## Check naming convention
The following function returns true if the naming convention is as expected, false otherwise.
| function|description|
|:--|:--|
|IsSnakeCase()| check whether string is snake_case style or not |
|IsChainCase()| check whether string is chain-case style or not|
|IsKebabCase()| same as IsChainCase()|
|IsCamelCase()| check whether string is camelCase style or not |
|IsPascalCase()| check whether string is camelCase style or not |
|IsFlatCase()| check whether string is flatcase style or not|
|IsUpperCase()| check whether string is UPPER_CASE style or not |  

If first character is digit, IsCamelCase(), IsPascalCase(), IsFlatCase() always returns false. Because function can not judge upper or lower.

# Example
```
package main

import (
	"fmt"

	"github.com/nao1215/nameconv"
)

func main() {
	fmt.Println(nameconv.ToSnakeCase("dave mustaine"))            // dave_mustaine
	fmt.Println(nameconv.ToChainCase("TifaLockhart"))             // tifa-lockhart
	fmt.Println(nameconv.ToKebabCase("The_Shawshank_Redemption")) // the-shawshank-redemption
	fmt.Println(nameconv.ToCamelCase("master-of_puppets"))        // masterOfPuppets
	fmt.Println(nameconv.ToPascalCase("Miracles_outOf-nowhere"))  // MiraclesOutOfNowhere
	fmt.Println(nameconv.ToFlatCase("SolBadguy"))                 // Sol badguy
	fmt.Println(nameconv.ToUpperCase("heaven and hell"))          // HEAVEN_AND_HELL

	fmt.Println(nameconv.IsSnakeCase("snake_case"))  // true
	fmt.Println(nameconv.IsChainCase("chain-case"))  // true
	fmt.Println(nameconv.IsKebabCase("kebab case"))  // false
	fmt.Println(nameconv.IsCamelCase("CamelCase"))   // false
	fmt.Println(nameconv.IsPascalCase("pascalCase")) // false
	fmt.Println(nameconv.IsFlatCase("flat-case"))    // false
	fmt.Println(nameconv.IsUpperCase("0_UPPER"))     // true
}
```
  
# Contact
If you would like to send comments such as "find a bug" or "request for additional features" to the developer, please use one of the following contacts.

[GitHub Issue](https://github.com/nao1215/gup/nameconv)

# LICENSE
The nameconv project is the mixed-license.

- MIT License（casee*.go and camelcase*.go）
- Apache License Version 2.0（All codes other than the above）

The authors of the MIT license source code are [pinzolo](https://github.com/pinzolo) and [Fatih Arslan](https://github.com/fatih). The code written by each author clearly states the full MIT license and Copyright.
