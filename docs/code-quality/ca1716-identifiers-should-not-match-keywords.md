---
title: "CA1716: Identifiers should not match keywords"
ms.date: 11/04/2016
ms.prod: visual-studio-dev15
ms.topic: reference
f1_keywords:
  - "IdentifiersShouldNotMatchKeywords"
  - "CA1716"
helpviewer_keywords:
  - "IdentifiersShouldNotMatchKeywords"
  - "CA1716"
ms.assetid: 900cc8a1-1089-4069-a4ce-10b109ac4fab
author: gewarren
ms.author: gewarren
manager: douge
ms.workload:
  - "multiple"
---
# CA1716: Identifiers should not match keywords

|||
|-|-|
|TypeName|IdentifiersShouldNotMatchKeywords|
|CheckId|CA1716|
|Category|Microsoft.Naming|
|Breaking Change|Breaking|

## Cause

A name of a namespace, a type, or a viritual or interface member matches a reserved keyword in a programming language.

## Rule description

Identifiers for namespaces, types, and virtual and interface members should not match keywords that are defined by languages that target the common language runtime. Depending on the language that is used and the keyword, compiler errors and ambiguities can make the library difficult to use.

This rule checks against keywords in the following languages:

- Visual Basic

- C#

- C++/CLI

Case-insensitive comparison is used for [!INCLUDE[vbprvb](../code-quality/includes/vbprvb_md.md)] keywords, and case-sensitive comparison is used for the other languages.

## How to fix violations

Select a name that does not appear in the list of keywords.

## When to suppress warnings

You can suppress a warning from this rule if you are convinced that the identifier will not confuse users of the API, and that  the library is usable in all available languages in the .NET Framework.