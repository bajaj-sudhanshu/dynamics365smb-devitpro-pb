---
title: "Blob.CreateOutStream(OutStream [, TextEncoding]) Method"
description: "Creates an OutStream object for a binary large object (BLOB)."
ms.author: solsen
ms.custom: na
ms.date: 10/29/2021
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: reference
author: SusanneWindfeldPedersen
---
[//]: # (START>DO_NOT_EDIT)
[//]: # (IMPORTANT:Do not edit any of the content between here and the END>DO_NOT_EDIT.)
[//]: # (Any modifications should be made in the .xml files in the ModernDev repo.)
# Blob.CreateOutStream(OutStream [, TextEncoding]) Method
> **Version**: _Available or changed with runtime version 1.0._

Creates an OutStream object for a binary large object (BLOB). This enables you to write data to the BLOB.


## Syntax
```AL
 Blob.CreateOutStream(OutStream: OutStream [, Encoding: TextEncoding])
```
## Parameters
*Blob*  
&emsp;Type: [Blob](blob-data-type.md)  
An instance of the [Blob](blob-data-type.md) data type.  

*OutStream*  
&emsp;Type: [OutStream](../outstream/outstream-data-type.md)  
The OutStream object type that has been created.
        
*[Optional] Encoding*  
&emsp;Type: [TextEncoding](../textencoding/textencoding-option.md)  
The encoding that will be used by the stream. The default encoding is MSDos.  



[//]: # (IMPORTANT: END>DO_NOT_EDIT)

 Optionally, you can specify the encoding on the stream. By specifying the [File Handling and Text Encoding](../../devenv-file-handling-and-text-encoding.md), you ensure that all the language-specific characters are represented correctly in [!INCLUDE[d365fin_md](../../includes/d365fin_md.md)] when you read data and write data. The following example illustrates how you can set the encoding to Windows when you create a stream for a BLOB field.  
  
```  
MyTable.MyBLOBfield.CreateOutStream(MyStream, TextEncoding::WINDOWS);  
```  
  
 For more information, see [File Handling and Text Encoding](../../devenv-file-handling-and-text-encoding.md).  

## See Also
[Blob Data Type](blob-data-type.md)  
[Get Started with AL](../../devenv-get-started.md)  
[Developing Extensions](../../devenv-dev-overview.md)