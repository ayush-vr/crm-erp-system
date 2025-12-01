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
├── features
│   ├── ar_eg_ملف_مفتوح_المصدر_مجاني_للبرمجيات_ERP_CRM.md
│   ├── bg_bg_свободен_отворен_източник_erp_crm_софтуер.md
│   ├── bn_bd_ফ্রি_ওপেন_সোর্স_ইআরপি_সিআরএম_সফটওয়্যার.md
│   ├── ca_es_software_erp_crm_de_codi_obert_gratuït.md
│   ├── cs_cz_volný_otevřený_zdroj_erp_crm_software.md
│   ├── da_dk_gratis_åben_kilde_erp_crm_software.md
│   ├── de_de_frei_offene_quelle_erp_crm_software.md
│   ├── el_gr_ελεύθερο_ανοικτο_πηγαίο_erp_crm_λογισμικό.md
│   ├── en_us_free_open_source_erp_crm_software.md
│   ├── es_es_software_erp_crm_de_código_abierto_y_gratis.md
│   ├── et_ee_tasuta_avatud_lähtekoodiga_erp_crm_tarkvara.md
│   ├── fa_ir_رایگان_منبع_باز_نرم‌افزار_مدیریت_مالی_و_ارتباطات.md
│   ├── fi_fi_ilmainen_avoin_lähdekoodi_erp_crm_ohjelmisto.md
│   ├── fr_fr_gratuit_logiciel_erp_crm_open_source.md
│   ├── hi_in_मुफ्त_खुला_स्रोत_ईआरपी_सीआरएम_सॉफ़्टवेयर.md
│   ├── hr_hr_besplatni_otvoreni_izvor_erp_crm_softver.md
│   ├── hu_hu_ingyenes_nyílt_forráskódú_erp_crm_szoftver.md
│   ├── id_id_perangkat_lunak_erp_crm_sumber_terbuka_gratis.md
│   ├── it_it_software_erp_crm_open_source_gratuito.md
│   ├── ja_jp_フリーオープンソースERP CRMソフトウェア.md
│   ├── ko_kr_자유_오픈_소스_ERP_CRM_소프트웨어.md
│   ├── lt_lt_nemokamas_atviras_kodo_erp_crm_programinė_įranga.md
│   ├── lv_lv_bezmaksas_atvērtā_koda_erp_crm_programmatūra.md
│   ├── mk_mk_фрее_опен_сорсе_ерп_црм_софтвер.md
│   ├── ms_my_fail_terbuka_sumber_erp_crm_perisian.md
│   ├── nb_no_gratis_åpen_kilde_erp_crm_programvare.md
│   ├── nl_nl_vrije_open_source_erp_crm_software.md
│   ├── pl_pl_bezpłatne_otwarte_źródło_erp_crm_oprogramowanie.md
│   ├── pt_br_software_de_erp_e_crm_de_código_aberto_gratuito.md
│   ├── pt_pt_software_de_erp_crm_de_código_aberto_gratuito.md
│   ├── ro_ro_software_erp_crm_open_source_gratuit.md
│   ├── ru_ru_бесплатное_открытое_программное_обеспечение_erp_crm.md
│   ├── sk_sk_zdarma_otvorene_zdrojove_erp_crm_software.md
│   ├── sl_si_brezplačni_odprtokodni_erp_crm_programski_oprema.md
│   ├── sr_rs_besplatni_otvoreni_izvor_erp_crm_softver.md
│   ├── sv_se_fri_öppen_källkods_erp_crm_programvara.md
│   ├── th_th_ฟรี_โปรแกรม_ตัวจัดการแหล่งข้อมูลโปรแกรม_ERP_CRM.md
│   ├── tr_tr_ücretsiz_açık_kaynak_erp_crm_yazılımı.md
│   ├── uk_ua_безкоштовне_відкрите_джерело_erp_crm_програмне_забезпечення.md
│   ├── ur_pk_مفت_کھولیں_سورس_erp_crm_سافٹ ویئر.md
│   ├── vi_vn_chương_trình_quản_lý_doanh_nghiệp_crm_nguồn_mở_miễn_phí.md
│   └── zh_cn_免费开源ERP CRM软件.md
├── frontend
│   ├── index.html
│   ├── jsconfig.json
│   ├── package.json
│   ├── public
│   │   └── robots.txt
│   ├── rollup.config.js
│   ├── src
│   │   ├── RootApp.jsx
│   │   ├── apps
│   │   │   ├── ErpApp.jsx
│   │   │   ├── Header
│   │   │   │   ├── HeaderContainer.jsx
│   │   │   │   └── UpgradeButton.jsx
│   │   │   ├── IdurarOs.jsx
│   │   │   └── Navigation
│   │   │       └── NavigationContainer.jsx
│   │   ├── auth
│   │   │   ├── auth.service.js
│   │   │   └── index.js
│   │   ├── components
│   │   │   ├── AutoCompleteAsync
│   │   │   │   └── index.jsx
│   │   │   ├── CollapseBox
│   │   │   │   └── index.jsx
│   │   │   ├── CreateForm
│   │   │   │   └── index.jsx
│   │   │   ├── CrudModal
│   │   │   │   └── index.jsx
│   │   │   ├── DataTable
│   │   │   │   └── DataTable.jsx
│   │   │   ├── DeleteModal
│   │   │   │   └── index.jsx
│   │   │   ├── IconMenu
│   │   │   │   └── index.jsx
│   │   │   ├── Loading
│   │   │   │   └── index.jsx
│   │   │   ├── MoneyInputFormItem
│   │   │   │   └── index.jsx
│   │   │   ├── MultiStepSelectAsync
│   │   │   │   └── index.jsx
│   │   │   ├── NotFound
│   │   │   │   └── index.jsx
│   │   │   ├── Notification
│   │   │   │   └── index.jsx
│   │   │   ├── PageLoader
│   │   │   │   └── index.jsx
│   │   │   ├── ReadItem
│   │   │   │   └── index.jsx
│   │   │   ├── SearchItem
│   │   │   │   └── index.jsx
│   │   │   ├── SelectAsync
│   │   │   │   └── index.jsx
│   │   │   ├── SelectTag
│   │   │   │   └── index.jsx
│   │   │   ├── SidePanel
│   │   │   │   └── index.jsx
│   │   │   ├── TabsContent
│   │   │   │   └── TabsContent.jsx
│   │   │   ├── Tag
│   │   │   │   └── index.jsx
│   │   │   ├── UpdateForm
│   │   │   │   └── index.jsx
│   │   │   ├── Visibility
│   │   │   │   └── index.jsx
│   │   │   └── outsideClick.js
│   │   │       ├── demo.js
│   │   │       └── index.js
│   │   ├── config
│   │   │   └── serverApiConfig.js
│   │   ├── context
│   │   │   ├── adavancedCrud
│   │   │   │   ├── actions.jsx
│   │   │   │   ├── index.jsx
│   │   │   │   ├── reducer.jsx
│   │   │   │   ├── selectors.jsx
│   │   │   │   └── types.jsx
│   │   │   ├── appContext
│   │   │   │   ├── actions.jsx
│   │   │   │   ├── index.jsx
│   │   │   │   ├── reducer.jsx
│   │   │   │   └── types.jsx
│   │   │   ├── crud
│   │   │   │   ├── actions.jsx
│   │   │   │   ├── index.jsx
│   │   │   │   ├── reducer.jsx
│   │   │   │   ├── selectors.jsx
│   │   │   │   └── types.jsx
│   │   │   ├── erp
│   │   │   │   ├── actions.jsx
│   │   │   │   ├── index.jsx
│   │   │   │   ├── reducer.jsx
│   │   │   │   ├── selectors.jsx
│   │   │   │   └── types.jsx
│   │   │   └── profileContext
│   │   │       ├── actions.jsx
│   │   │       ├── index.jsx
│   │   │       ├── reducer.jsx
│   │   │       ├── selectors.jsx
│   │   │       └── types.jsx
│   │   ├── favicon.ico
│   │   ├── forms
│   │   │   ├── AdminForm.jsx
│   │   │   ├── AdvancedSettingsForm.jsx
│   │   │   ├── CurrencyForm.jsx
│   │   │   ├── CustomerForm.jsx
│   │   │   ├── DynamicForm
│   │   │   │   └── index.jsx
│   │   │   ├── EmployeeForm.jsx
│   │   │   ├── ForgetPasswordForm.jsx
│   │   │   ├── InventoryForm.jsx
│   │   │   ├── LeadForm.jsx
│   │   │   ├── LoginForm.jsx
│   │   │   ├── OrderForm.jsx
│   │   │   ├── PaymentForm.jsx
│   │   │   ├── PaymentModeForm.jsx
│   │   │   ├── RegisterForm.jsx
│   │   │   ├── ResetPasswordForm.jsx
│   │   │   ├── TaxForm.jsx
│   │   │   └── UpdateEmail.jsx
│   │   ├── hooks
│   │   │   ├── useDebounce.jsx
│   │   │   ├── useFetch.jsx
│   │   │   ├── useMail.jsx
│   │   │   ├── useNetwork.jsx
│   │   │   ├── useOnFetch.jsx
│   │   │   ├── useResponsive.jsx
│   │   │   └── useTimeoutFn.jsx
│   │   ├── layout
│   │   │   ├── AuthLayout
│   │   │   │   └── index.jsx
│   │   │   ├── CrudLayout
│   │   │   │   └── index.jsx
│   │   │   ├── DashboardLayout
│   │   │   │   └── index.jsx
│   │   │   ├── DefaultLayout
│   │   │   │   └── index.jsx
│   │   │   ├── ErpLayout
│   │   │   │   └── index.jsx
│   │   │   ├── Footer
│   │   │   │   └── index.jsx
│   │   │   ├── ProfileLayout
│   │   │   │   └── index.jsx
│   │   │   ├── SettingsLayout
│   │   │   │   └── index.jsx
│   │   │   └── index.jsx
│   │   ├── locale
│   │   │   ├── Localization.jsx
│   │   │   ├── antdLocale.js
│   │   │   ├── coreTranslation.js
│   │   │   ├── translation
│   │   │   │   ├── en_us.js
│   │   │   │   ├── otherTranslation.js
│   │   │   │   └── translation.js
│   │   │   └── useLanguage.jsx
│   │   ├── logo-icon.svg
│   │   ├── main.jsx
│   │   ├── modules
│   │   │   ├── AuthModule
│   │   │   │   ├── SideContent.jsx
│   │   │   │   └── index.jsx
│   │   │   ├── CrudModule
│   │   │   │   └── CrudModule.jsx
│   │   │   ├── DashboardModule
│   │   │   │   ├── components
│   │   │   │   │   ├── CustomerPreviewCard.jsx
│   │   │   │   │   ├── PreviewCard.jsx
│   │   │   │   │   ├── RecentTable
│   │   │   │   │   │   └── index.jsx
│   │   │   │   │   └── SummaryCard.jsx
│   │   │   │   └── index.jsx
│   │   │   ├── ErpPanelModule
│   │   │   │   ├── CreateItem.jsx
│   │   │   │   ├── DataTable.jsx
│   │   │   │   ├── DeleteItem.jsx
│   │   │   │   ├── ItemRow.jsx
│   │   │   │   ├── ReadItem.jsx
│   │   │   │   ├── SearchItem.jsx
│   │   │   │   ├── UpdateItem.jsx
│   │   │   │   └── index.jsx
│   │   │   ├── InvoiceModule
│   │   │   │   ├── CreateInvoiceModule
│   │   │   │   │   └── index.jsx
│   │   │   │   ├── Forms
│   │   │   │   │   └── InvoiceForm.jsx
│   │   │   │   ├── InvoiceDataTableModule
│   │   │   │   │   └── index.jsx
│   │   │   │   ├── ReadInvoiceModule
│   │   │   │   │   └── index.jsx
│   │   │   │   ├── RecordPaymentModule
│   │   │   │   │   ├── components
│   │   │   │   │   │   ├── Payment.jsx
│   │   │   │   │   │   └── RecordPayment.jsx
│   │   │   │   │   └── index.jsx
│   │   │   │   └── UpdateInvoiceModule
│   │   │   │       └── index.jsx
│   │   │   ├── PaymentModule
│   │   │   │   ├── PaymentDataTableModule
│   │   │   │   │   └── index.jsx
│   │   │   │   ├── ReadPaymentModule
│   │   │   │   │   ├── components
│   │   │   │   │   │   └── ReadItem.jsx
│   │   │   │   │   └── index.jsx
│   │   │   │   └── UpdatePaymentModule
│   │   │   │       ├── components
│   │   │   │       │   ├── Payment.jsx
│   │   │   │       │   └── UpdatePayment.jsx
│   │   │   │       └── index.jsx
│   │   │   ├── ProfileModule
│   │   │   │   ├── components
│   │   │   │   │   ├── AdminInfo.jsx
│   │   │   │   │   ├── PasswordModal.jsx
│   │   │   │   │   ├── Profile.jsx
│   │   │   │   │   ├── ProfileAdminForm.jsx
│   │   │   │   │   ├── UpdateAdmin.jsx
│   │   │   │   │   └── UploadImg.jsx
│   │   │   │   └── index.jsx
│   │   │   ├── QuoteModule
│   │   │   │   ├── CreateQuoteModule
│   │   │   │   │   └── index.jsx
│   │   │   │   ├── Forms
│   │   │   │   │   └── QuoteForm.jsx
│   │   │   │   ├── QuoteDataTableModule
│   │   │   │   │   └── index.jsx
│   │   │   │   ├── ReadQuoteModule
│   │   │   │   │   └── index.jsx
│   │   │   │   └── UpdateQuoteModule
│   │   │   │       └── index.jsx
│   │   │   └── SettingModule
│   │   │       ├── CompanyLogoSettingsModule
│   │   │       │   ├── forms
│   │   │       │   │   └── AppSettingForm.jsx
│   │   │       │   └── index.jsx
│   │   │       ├── CompanySettingsModule
│   │   │       │   ├── SettingsForm.jsx
│   │   │       │   └── index.jsx
│   │   │       ├── FinanceSettingsModule
│   │   │       │   ├── SettingsForm.jsx
│   │   │       │   └── index.jsx
│   │   │       ├── GeneralSettingsModule
│   │   │       │   ├── forms
│   │   │       │   │   └── GeneralSettingForm.jsx
│   │   │       │   └── index.jsx
│   │   │       ├── MoneyFormatSettingsModule
│   │   │       │   ├── SettingsForm.jsx
│   │   │       │   └── index.jsx
│   │   │       └── components
│   │   │           ├── SetingsSection.jsx
│   │   │           ├── UpdateSettingForm.jsx
│   │   │           └── UpdateSettingModule.jsx
│   │   ├── pages
│   │   │   ├── About.jsx
│   │   │   ├── Customer
│   │   │   │   ├── config.js
│   │   │   │   └── index.jsx
│   │   │   ├── Dashboard.jsx
│   │   │   ├── ForgetPassword.jsx
│   │   │   ├── Invoice
│   │   │   │   ├── InvoiceCreate.jsx
│   │   │   │   ├── InvoiceRead.jsx
│   │   │   │   ├── InvoiceRecordPayment.jsx
│   │   │   │   ├── InvoiceUpdate.jsx
│   │   │   │   └── index.jsx
│   │   │   ├── Login.jsx
│   │   │   ├── Logout.jsx
│   │   │   ├── NotFound.jsx
│   │   │   ├── Payment
│   │   │   │   ├── PaymentRead.jsx
│   │   │   │   ├── PaymentUpdate.jsx
│   │   │   │   └── index.jsx
│   │   │   ├── PaymentMode
│   │   │   │   └── index.jsx
│   │   │   ├── Profile.jsx
│   │   │   ├── Quote
│   │   │   │   ├── QuoteCreate.jsx
│   │   │   │   ├── QuoteRead.jsx
│   │   │   │   ├── QuoteUpdate.jsx
│   │   │   │   └── index.jsx
│   │   │   ├── ResetPassword.jsx
│   │   │   ├── Settings
│   │   │   │   ├── CompanyLogoSettings.jsx
│   │   │   │   ├── CompanySettings.jsx
│   │   │   │   ├── FinanceSettings.jsx
│   │   │   │   ├── GeneralSettings.jsx
│   │   │   │   ├── MoneyFormatSettings.jsx
│   │   │   │   └── Settings.jsx
│   │   │   └── Taxes
│   │   │       └── index.jsx
│   │   ├── redux
│   │   │   ├── adavancedCrud
│   │   │   │   ├── actions.js
│   │   │   │   ├── index.js
│   │   │   │   ├── reducer.js
│   │   │   │   ├── selectors.js
│   │   │   │   └── types.js
│   │   │   ├── auth
│   │   │   │   ├── actions.js
│   │   │   │   ├── index.js
│   │   │   │   ├── reducer.js
│   │   │   │   ├── selectors.js
│   │   │   │   └── types.js
│   │   │   ├── crud
│   │   │   │   ├── actions.js
│   │   │   │   ├── index.js
│   │   │   │   ├── reducer.js
│   │   │   │   ├── selectors.js
│   │   │   │   └── types.js
│   │   │   ├── erp
│   │   │   │   ├── actions.js
│   │   │   │   ├── index.js
│   │   │   │   ├── reducer.js
│   │   │   │   ├── selectors.js
│   │   │   │   └── types.js
│   │   │   ├── rootReducer.js
│   │   │   ├── settings
│   │   │   │   ├── actions.js
│   │   │   │   ├── index.js
│   │   │   │   ├── reducer.js
│   │   │   │   ├── selectors.js
│   │   │   │   └── types.js
│   │   │   ├── store.js
│   │   │   └── storePersist.js
│   │   ├── request
│   │   │   ├── checkImage.js
│   │   │   ├── codeMessage.js
│   │   │   ├── errorHandler.js
│   │   │   ├── index.js
│   │   │   ├── request.js
│   │   │   └── successHandler.js
│   │   ├── router
│   │   │   ├── AppRouter.jsx
│   │   │   ├── AuthRouter.jsx
│   │   │   └── routes.jsx
│   │   ├── settings
│   │   │   ├── index.jsx
│   │   │   ├── useDate.jsx
│   │   │   └── useMoney.jsx
│   │   ├── style
│   │   │   ├── app.css
│   │   │   ├── images
│   │   │   │   ├── checklist.svg
│   │   │   │   ├── fitbit-gray.svg
│   │   │   │   ├── flow-xo-gray.svg
│   │   │   │   ├── gitlab-gray.svg
│   │   │   │   ├── idurar-crm-erp.svg
│   │   │   │   ├── layar-gray.svg
│   │   │   │   ├── logo-icon.png
│   │   │   │   ├── logo-icon.svg
│   │   │   │   ├── logo-menu.png
│   │   │   │   ├── logo-text.png
│   │   │   │   ├── logo-text.svg
│   │   │   │   ├── logo.png
│   │   │   │   ├── logo.svg
│   │   │   │   ├── logo1.png
│   │   │   │   ├── logo2.png
│   │   │   │   ├── logo3.png
│   │   │   │   ├── logo4.png
│   │   │   │   └── photo.png
│   │   │   └── partials
│   │   │       ├── auth.css
│   │   │       ├── collapseBox.css
│   │   │       ├── core.css
│   │   │       ├── customAntd.css
│   │   │       ├── erp.css
│   │   │       ├── header.css
│   │   │       ├── layout.css
│   │   │       ├── navigation.css
│   │   │       ├── rest.css
│   │   │       ├── sidePanel.css
│   │   │       └── transition.css
│   │   └── utils
│   │       ├── calculate.js
│   │       ├── color.js
│   │       ├── countryList.js
│   │       ├── currencyList.js
│   │       ├── dataStructure.jsx
│   │       ├── helpers.js
│   │       ├── isBrowser.js
│   │       ├── statusTagColor.js
│   │       ├── tagColor.js
│   │       └── valueType.js
│   ├── temp.env
│   └── vite.config.js
├── idurar-crm-erp.svg
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

Please ensure your code follows the project's style guidelines and includes tests where applicable.

## 📜 License

This project is licensed under the Fair-code License License.

---
*This README was generated with ❤️ by ReadmeBuddy*
