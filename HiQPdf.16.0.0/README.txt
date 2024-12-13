HiQPdf Library for .NET
=======================

HiQPdf Library for .NET offers you a modern, simple, fast, flexible and powerful tool to create complex and stylish PDF documents in .NET applications with just a few lines of C# code.

HiQPdf library includes the fastest and the most precise HTML to PDF conversion technology. You can easily design a document in HTML with CSS3, JavaScript, SVG or Web Fonts and then convert it to PDF preserving the exact content and style.

The library is much more than just a HTML to PDF converter. It is a complete PDF library that you can use to create new PDF documents and edit existing PDF documents, extract text and images from PDF, search text in PDF, rasterize PDF pages to images or convert PDF to HTML.
You can find more details accessing the product web page at http://www.hiqpdf.com/html-to-pdf-library.aspx .

This library is compatible with .NET Framework for Windows 32-bit (x86) and 64-bit (x64) operating systems. The NuGet package optimized for x64 is HiQPdf.x64 .

The NuGet packages for .NET Core and .NET Standard are HiQPdf.NetCore and HiQPdf.NetCore.x64 .

For Linux, MacOS, Azure App Service, Xamarin, UWP or any other platform for .NET you can use the multi-platform HiQPdf.Client NuGet package. 
See the http://www.hiqpdf.com/multiplatform-html-to-pdf-library-net-core.aspx page for more details.

Library Features
================

* HTML to PDF Converter to quickly create with very high accuracy PDF documents from HTML documents with advanced support for CSS, JavaScript, Web Fonts and SVG. The converter can automatically create table of contents, bookmarks and internal links from HTML document structure
* HTML to Image Converter to take snapshots of web pages and produce raster images in various formats like PNG, JPG, BMP
* HTML to SVG Converter to create high quality vector images in SVG  format from HTML
* PDF to Image Converter allows you to rasterize PDF document pages to images and produce a separate image for each PDF page or to create a multi-page TIFF image for the entire PDF document
* PDF to HTML Converter offers the possibility to create HTML documents from PDF pages and also to produce a index file for the entire document
* PDF to Text Converter can extract the text from PDF documents with various options like preserving the original text order or the reading order, marking the page breaks with special characters 
* Search text in PDF functionality allows you to search and highlight text in PDF document pages
* Extract images from PDF to get the images embedded in PDF documents preserving images transparency
* Create PDF Documents in a classic manner laying out PDF objects like text, HTML, SVG, images and graphics to an empty document
* Security and Digital Signatures feature allows you create encrypted, password protected, digitally signed PDF documents
* Interactive Features like PDF forms, text notes, internal links, JavaScript actions
* Merge PDF feature allows you combine multiple PDF documents into a single one
* Stamp PDF to apply HTML, text and images content which repeats in each PDF page of a PDF document

Compatible Platforms
====================

HiQPdf Library for .NET has builds for .NET Framework 4.0 and .NET Framework 2.0 and its compatibility list includes:

* .NET Framework 4.8.1, 4.7.2, 4.6.1, 4.0, 3.5, 2.0 and the later versions
* Windows 32-bit (x86) and 64-bit (x64) operating systems
* Azure Cloud Services, Azure Virtual Machines
* Web, Desktop and Console applications for .NET Framework

Start Using HiQPdf
==================

You can start by copying the C# code below in your application or you can start with our demo applications for .NET from downloadable product packages.

C# Code Samples for HTML to PDF
-------------------------------

The C# code samples below show how to quickly produce PDF documents from HTML pages or HTML code and save the resulted PDF to a memory buffer, to a PDF file or send it to browser for download when created in ASP.NET applications.

At the top of your C# source file you have to add the 'using HiQPdf;' instruction to make available the HiQPdf namespace to your application code.

    // Include the HiQPdf namespace at the top of your C# file
    using HiQPdf;

You can use the C# code below to convert a HTML code or a HTML page from a given URL to a PDF file.

    // Create the HTML to PDF converter object
    HtmlToPdf converter = new HtmlToPdf();
    
    // Convert the HTML code to a PDF file
    converter.ConvertHtmlToFile("<b>Hello World</b> from HiQPdf !", null, "html_to_file.pdf");
    
    // Convert the HTML page from URL to a PDF file
    string urlToConvert = "http://www.hiqpdf.com";
    converter.ConvertUrlToFile(urlToConvert, "url_to_file.pdf");

Alternatively you can produce the PDF document in a memory buffer that you can further save to a file on server.

    // Create the HTML to PDF converter object
    HtmlToPdf converter = new HtmlToPdf();
    
    // Convert the HTML code to memory
    byte[] htmlToPdfData = converter.ConvertHtmlToMemory("<b>Hello World</b> from HiQPdf !", null);
    
    // Save the PDF data to a file
    System.IO.File.WriteAllBytes("html_to_memory.pdf", htmlToPdfData);
    
    // Convert the HTML page from URL to memory
    string urlToConvert = "http://www.hiqpdf.com";
    byte[] urlToPdfData = converter.ConvertUrlToMemory(urlToConvert);
    
    // Save the PDF data to a file
    System.IO.File.WriteAllBytes("url_to_memory.pdf", urlToPdfData);

The C# code below can be used in your ASP.NET Core and ASP.NET MVC applications to convert a HTML code to PDF in a memory buffer and then send the PDF data for download to browser.

    // Create the HTML to PDF converter object
    HtmlToPdf converter = new HtmlToPdf();
    
    // Convert the HTML code to memory
    byte[] htmlToPdfData = converter.ConvertHtmlToMemory("<b>Hello World</b> from HiQPdf !", null);
    
    FileResult fileResult = new FileContentResult(htmlToPdfData, "application/pdf");
    fileResult.FileDownloadName = "html_to_pdf.pdf";
    return fileResult;

The C# code below can be used in your ASP.NET Web Forms applications to convert a HTML code to PDF in a memory buffer and then send the PDF data for download to browser.

    // Create the HTML to PDF converter object
    HtmlToPdf converter = new HtmlToPdf();
    
    // Convert the HTML code to memory
    byte[] htmlToPdfData = converter.ConvertHtmlToMemory("<b>Hello World</b> from HiQPdf !", null);
    
    HttpResponse httpResponse = HttpContext.Current.Response;
    httpResponse.AddHeader("Content-Type", "application/pdf");
    httpResponse.AddHeader("Content-Disposition",
        String.Format("attachment; filename=html_to_pdf.pdf; size={0}",
        htmlToPdfData.Length.ToString()));
    httpResponse.BinaryWrite(htmlToPdfData);
    httpResponse.End();

Free Trial Download
===================

You can download free trial packages for .NET Framework and .NET Core from http://www.hiqpdf.com/downloads.aspx web page.

The free trial package for .NET Framework contains the library binaries, ASP.NET demo applications for Web Forms and for MVC with C# code for all library features, Windows Forms demo applications for C# and VB.NET, an Azure Cloud Service Web Role demo, the complete product documentation with examples and API reference.

Licensing
=========

The licensing model is simple and flexible. The licenses are perpetual and there is no limit for the number of machines where you can deploy your applications using the HiQPdf library.
You can find more details about licensing on http://www.hiqpdf.com/purchase.aspx web page.

Support
=======

For support and questions please use the email addresses from the http://www.hiqpdf.com/contact.aspx web page. 
