# crm-erp-system


## 📝 Description

This project is a CRM-ERP system built with Express.js. It provides core functionalities like authentication and a web interface, offering a foundation for managing customer relationships and enterprise resource planning. The system is designed to be modular and scalable, allowing for future expansion and customization to meet specific business needs. It can be used as a starting point for building a comprehensive CRM-ERP solution or integrated with other systems.

## ✨ Features

- 🔐 Auth
- 🕸️ Web


## 🛠️ Tech Stack

- 🚀 Express.js


## 📦 Key Dependencies

```
@aws-sdk/client-s3: ^3.509.0
bcryptjs: ^2.4.3
compression: ^1.7.4
cookie-parser: ^1.4.6
cors: ^2.8.5
currency.js: 2.0.4
dotenv: 16.3.1
express: ^4.18.2
express-fileupload: ^1.4.3
express-rate-limit: ^7.1.5
glob: 10.3.10
html-pdf: ^3.0.1
joi: ^17.11.0
jsonwebtoken: ^9.0.2
lodash: ^4.17.21
```

## 🚀 Run Commands

- **start**: `npm run start`
- **dev**: `npm run dev`
- **production**: `npm run production`
- **setup**: `npm run setup`
- **upgrade**: `npm run upgrade`
- **reset**: `npm run reset`


## 📁 Project Structure

```
.
├── CODE-OF-CONDUCT.md
├── CONTRIBUTING.md
├── INSTALLATION-INSTRUCTIONS.md
├── LICENSE
├── SECURITY.md
├── backend
│   ├── jsconfig.json
│   ├── package.json
│   └── src
│       ├── app.js
│       ├── controllers
│       │   ├── appControllers
│       │   │   ├── clientController
│       │   │   │   ├── index.js
│       │   │   │   └── summary.js
│       │   │   ├── index.js
│       │   │   ├── invoiceController
│       │   │   │   ├── create.js
│       │   │   │   ├── index.js
│       │   │   │   ├── paginatedList.js
│       │   │   │   ├── read.js
│       │   │   │   ├── remove.js
│       │   │   │   ├── schemaValidate.js
│       │   │   │   ├── sendMail.js
│       │   │   │   ├── summary.js
│       │   │   │   └── update.js
│       │   │   ├── paymentController
│       │   │   │   ├── create.js
│       │   │   │   ├── index.js
│       │   │   │   ├── remove.js
│       │   │   │   ├── sendMail.js
│       │   │   │   ├── summary.js
│       │   │   │   └── update.js
│       │   │   ├── paymentModeController
│       │   │   │   └── index.js
│       │   │   ├── quoteController
│       │   │   │   ├── convertQuoteToInvoice.js
│       │   │   │   ├── create.js
│       │   │   │   ├── index.js
│       │   │   │   ├── paginatedList.js
│       │   │   │   ├── read.js
│       │   │   │   ├── sendMail.js
│       │   │   │   ├── summary.js
│       │   │   │   └── update.js
│       │   │   └── taxesController
│       │   │       └── index.js
│       │   ├── coreControllers
│       │   │   ├── adminAuth
│       │   │   │   └── index.js
│       │   │   ├── adminController
│       │   │   │   └── index.js
│       │   │   ├── settingController
│       │   │   │   ├── index.js
│       │   │   │   ├── listAll.js
│       │   │   │   ├── listBySettingKey.js
│       │   │   │   ├── readBySettingKey.js
│       │   │   │   ├── updateBySettingKey.js
│       │   │   │   └── updateManySetting.js
│       │   │   └── setup.js
│       │   ├── middlewaresControllers
│       │   │   ├── createAuthMiddleware
│       │   │   │   ├── authUser.js
│       │   │   │   ├── checkAndCorrectURL.js
│       │   │   │   ├── forgetPassword.js
│       │   │   │   ├── index.js
│       │   │   │   ├── isValidAuthToken.js
│       │   │   │   ├── login.js
│       │   │   │   ├── logout.js
│       │   │   │   ├── resetPassword.js
│       │   │   │   └── sendMail.js
│       │   │   ├── createCRUDController
│       │   │   │   ├── create.js
│       │   │   │   ├── filter.js
│       │   │   │   ├── index.js
│       │   │   │   ├── listAll.js
│       │   │   │   ├── paginatedList.js
│       │   │   │   ├── read.js
│       │   │   │   ├── remove.js
│       │   │   │   ├── search.js
│       │   │   │   ├── summary.js
│       │   │   │   └── update.js
│       │   │   └── createUserController
│       │   │       ├── index.js
│       │   │       ├── read.js
│       │   │       ├── updatePassword.js
│       │   │       ├── updateProfile.js
│       │   │       └── updateProfilePassword.js
│       │   └── pdfController
│       │       └── index.js
│       ├── emailTemplate
│       │   ├── SendEmailTemplate.js
│       │   └── emailVerfication.js
│       ├── handlers
│       │   ├── downloadHandler
│       │   │   └── downloadPdf.js
│       │   └── errorHandlers.js
│       ├── helpers.js
│       ├── locale
│       │   ├── languages.js
│       │   ├── translation
│       │   │   └── en_us.js
│       │   └── useLanguage.js
│       ├── middlewares
│       │   ├── inventory
│       │   │   ├── generateUniqueNumber.js
│       │   │   └── index.js
│       │   ├── serverData.js
│       │   ├── settings
│       │   │   ├── increaseBySettingKey.js
│       │   │   ├── index.js
│       │   │   ├── listAllSettings.js
│       │   │   ├── listBySettingKey.js
│       │   │   ├── loadSettings.js
│       │   │   ├── readBySettingKey.js
│       │   │   └── updateBySettingKey.js
│       │   └── uploadMiddleware
│       │       ├── DoSingleStorage.js
│       │       ├── LocalSingleStorage.js
│       │       ├── index.js
│       │       ├── singleStorageUpload.js
│       │       └── utils
│       │           ├── LocalfileFilter.js
│       │           └── fileFilterMiddleware.js
│       ├── models
│       │   ├── appModels
│       │   │   ├── Client.js
│       │   │   ├── Invoice.js
│       │   │   ├── Payment.js
│       │   │   ├── PaymentMode.js
│       │   │   ├── Quote.js
│       │   │   └── Taxes.js
│       │   ├── coreModels
│       │   │   ├── Admin.js
│       │   │   ├── AdminPassword.js
│       │   │   ├── Setting.js
│       │   │   └── Upload.js
│       │   └── utils
│       │       └── index.js
│       ├── pdf
│       │   ├── Invoice.pug
│       │   ├── Offer.pug
│       │   ├── Payment.pug
│       │   └── Quote.pug
│       ├── public
│       │   └── uploads
│       │       ├── admin
│       │       │   └── idurar-icon-png-80-i1kez.png
│       │       └── setting
│       │           └── company-logo.png
│       ├── routes
│       │   ├── appRoutes
│       │   │   └── appApi.js
│       │   └── coreRoutes
│       │       ├── coreApi.js
│       │       ├── coreAuth.js
│       │       ├── coreDownloadRouter.js
│       │       └── corePublicRouter.js
│       ├── server.js
│       ├── settings
│       │   ├── index.js
│       │   ├── useAppSettings.js
│       │   ├── useDate.js
│       │   └── useMoney.js
│       ├── setup
│       │   ├── defaultSettings
│       │   │   ├── appSettings.json
│       │   │   ├── clientSettings.json
│       │   │   ├── companySettings.json
│       │   │   ├── financeSettings.json
│       │   │   ├── invoiceSettings.json
│       │   │   ├── moneyFormatSettings.json
│       │   │   └── quoteSettings.json
│       │   ├── reset.js
│       │   ├── setup.js
│       │   └── setupConfig.json
│       └── utils
│           ├── countryList.js
│           ├── currency.js
│           ├── currencyList.js
│           └── is-path-inside.js
├── doc
│   ├── README.fr.md
│   └── README.sp.md
└── image.png
```

## 👥 Contributing

Contributions are welcome! Here's how you can help:

1. **Fork** the repository
2. **Clone** your fork: `git clone https://github.com/ayush-vr/crm-erp-system.git`
3. **Create** a new branch: `git checkout -b feature/your-feature`
4. **Commit** your changes: `git commit -am 'Add some feature'`
5. **Push** to your branch: `git push origin feature/your-feature`
6. **Open** a pull request

