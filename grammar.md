# SLPMoose grammar

The grammar for the SLPMoose esoteric programming language

Where:
- *Terminal symbols* are denoted by [Hyperlinks](https://en.wikipedia.org/wiki/Hyperlink)
- *Nonterminal symbols* are denoted by `code`
- *Regular expressions* are denoted by `r#"code"#` (Rust syntax)
- The given string is a single line/command containing no newlines
- There can be any non-zero amount of whitespace between tokens

## Command

→ `pursue` [Object](#object)  
→ `dub` [Object](#object) [StringLiteral](#stringliteral)  
→ `make` [Object](#object) [ObjectCommand](#objectcommand)  
→ `feed` [Object](#object)  
→ `send` [Object](#object) [ToPosition](#toposition)  
→ `send` [Object](#object) [List](#list)  
→ `count` [List](#list)

## Object

→ [StringLiteral](#stringliteral)  
→ `the` [List](#list)  
→ `any` [List](#list)

## List

→ [AtPosition](#atposition)  
→ `the` [PluralList](#plurallist)  
→ `any` [PluralList](#plurallist)  
→ [ListQualifier](#listqualifier) [List](#list)

## PluralList

→ [PluralType](#pluraltype)  
→ [PluralType](#pluraltype) [AtPosition](#atposition)  
→ [ListQualifier](#listqualifier) [PluralList](#plurallist)

## AtPosition

→ `at` [Position](#position)

## ToPosition

→ `to` [Position](#position)

## Position

→ `here`

## ListQualifier

→ [Type](#type)  
→ [Gender](#gender)  
→ [Status](#status)

## StringLiteral

→ `r#""(\\.|[^\\"])+""#`

## ObjectCommand

→ `bellow`  
→ `groan`  
→ `plagiarize`

## Type

→ `moose`  
→ `calf`  
→ `wolf`

## PluralType

→ `mooses`  
→ `calves`  
→ `wolves`

## Gender

→ `bull`  
→ `cow`  
→ `male`  
→ `female`

## Status

→ `alpha`  
→ `beta`  
→ `delta`  
→ `omega`
