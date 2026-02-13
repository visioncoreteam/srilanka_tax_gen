# Sri Lanka Invoice Generator

This application is a **Manager.io** extension that automatically generates invoice numbers compliant with **Sri Lanka Tax Department Guidelines**. It provides seamless integration with Manager.io accounting software to ensure your invoicing meets Sri Lankan tax regulations.

Please visit this link to go Live: **[Sri Lanka Invoice Generator Live](#)** _(Add your deployment URL here)_

## Table of Contents
- [What is Sri Lanka Invoice Generator?](#what-is-sri-lanka-invoice-generator)
- [Key Features](#key-features)
- [Invoice Number Format](#invoice-number-format)
- [Prerequisites](#prerequisites)
- [First-Time Setup](#first-time-setup)
- [How It Works](#how-it-works)
- [Technical Stack](#technical-stack)
- [Installation](#installation)
- [Project Structure](#project-structure)
- [Development](#development)
- [Video Demonstration](#video-demonstration)
- [Contributing](#contributing)
- [License](#license)
- [Support](#support)

---

## What is Sri Lanka Invoice Generator?

The **Sri Lanka Invoice Generator** is a web-based extension designed to work with Manager.io accounting software. It automates the generation of tax-compliant invoice numbers according to **Sri Lanka Tax Department** standards.

### Why Use This Application?
- **Compliance**: Ensures all invoice numbers follow Sri Lankan tax regulations
- **Automation**: Eliminates manual invoice numbering errors
- **Consistency**: Maintains sequential numbering with monthly resets
- **Integration**: Seamlessly works with Manager.io's custom fields system

The application addresses the need for standardized invoice numbering in Sri Lanka's business environment, helping businesses maintain proper documentation for tax purposes and audits.

---

## Key Features

✅ **Automatic Invoice Number Generation** - Creates compliant invoice numbers based on Sri Lankan tax regulations  
✅ **Monthly Sequential Numbering** - Resets sequence counter every month automatically  
✅ **Smart Sequence Detection** - Intelligently identifies the last invoice and continues the sequence  
✅ **Custom Business ID** - Integrates your company identifier into each invoice number  
✅ **Manager.io Integration** - Works directly with Manager.io's custom fields system  
✅ **Tax Department Compliant** - Follows official Sri Lanka Tax Department formatting standards

---

## Invoice Number Format

The application generates invoice numbers using the following standardized format:

```
YYMMM_[CompanyID]_XXXX
```

### Format Breakdown

| Component | Description | Example |
|-----------|-------------|---------|
| **YY** | Last 2 digits of the year | `26` (for 2026) |
| **MMM** | 3-letter month abbreviation | `JAN`, `FEB`, `MAR` |
| **CompanyID** | Your unique business identifier | `VISCO`, `ABC`, `XYZ` |
| **XXXX** | 4-digit sequential number (resets monthly) | `0001`, `0002`, `0003` |

### Example Invoice Numbers

- `26FEB_VISCO_0001` - First invoice in February 2026 for company "VISCO"
- `26FEB_VISCO_0002` - Second invoice in February 2026 for company "VISCO"
- `26MAR_ABC_0001` - First invoice in March 2026 for company "ABC" (sequence reset)

---

## First-Time Setup

⚠️ **Important**: You must configure your Company ID before generating invoices. Follow these steps:

### Step 1: Navigate to Settings
In Manager.io, go to:
```
Settings → Business Details
```

### Step 2: Locate the CompanyID Field
Find the custom field labeled `CompanyID` (automatically created by this extension)

### Step 3: Enter Your Business Code
Enter your unique business identifier:
- **Format**: Uppercase letters only
- **Length**: 3-6 characters recommended
- **Examples**: `VISCO`, `ABC`, `XYZ`, `TECHCO`

💡 **Tip**: This identifier will appear in all your invoice numbers, so choose something that represents your business clearly.

### Step 4: Save and Start Generating
Click **Save** in Manager.io, and you're ready to generate compliant invoice numbers!

⛔ **Warning**: Invoice generation will not work until the CompanyID field is populated. This is a mandatory requirement.

---

## How It Works

1. **Initial Setup**: The extension creates a custom field called `CompanyID` in your Manager.io business details
2. **Invoice Creation**: When you create a new invoice, the system:
   - Checks your last invoice number
   - Extracts the date and sequence number
   - Determines if a new month has started
   - Generates the next sequential number (or resets to 0001 for a new month)
3. **Automatic Formatting**: The invoice number is formatted according to Sri Lankan tax standards
4. **Seamless Integration**: The generated number is applied to your invoice in Manager.io

### Monthly Reset Logic
- When the month changes, the sequence automatically resets to `0001`
- Example: `26FEB_VISCO_0152` → `26MAR_VISCO_0001` (new month)

---

## Technical Stack

- **Framework**: ASP.NET Core MVC (.NET 8.0)
- **Language**: C# 14.0
- **Target Platform**: .NET 10
- **Frontend**: Razor Pages with Tailwind CSS
- **Styling**: Tailwind CSS (with custom configuration)
- **Integration**: Manager.io API/Custom Fields
- **Build Tools**: npm for CSS processing

---

## Video Demonstration

Watch this video to see how to set up and use the Sri Lanka Invoice Generator:

[![Sri Lanka Invoice Generator Demo]](https://youtu.be/zWvC9jmm7BE)

*Click the thumbnail above to watch the full setup and usage guide on YouTube.*

---


## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## Support

For issues, questions, or feature requests:

- **Issues**: Open an issue on Manager Forum
- **Email**: visioncoretechnologies@gmail.com
- **Documentation**: Refer to this README or inline code comments

### Common Issues

**Q: Invoice generation fails**  
A: Ensure the CompanyID field is populated in Manager.io Settings → Business Details


## Acknowledgments

- **Sri Lanka Tax Department** for providing invoice numbering guidelines
- **Manager.io** for the excellent accounting platform
- The open-source community for various tools and libraries used in this project

---

## Roadmap

**Made with ❤️ for Sri Lankan businesses**

---
