# GraphQL API Docs

- [Queries](#queries)
- [Mutations](#mutations)
- [Objects](#objects)

## Queries
- [agreement](#agreement)
- [availableBoxes](#availableboxes)
- [cities](#cities)
- [completedStorages](#completedstorages)
- [contacts](#contacts)
- [countryCodes](#countrycodes)
- [locksWithStaffAccess](#lockswithstaffaccess)
- [loginByCode](#loginbycode)
- [loginByPassword](#loginbypassword)
- [myBills](#mybills)
- [myBoxes](#myboxes)
- [myEvents](#myevents)
- [myStorages](#mystorages)
- [myUnits](#myunits)
- [offices](#offices)
- [order](#order)
- [ping](#ping)
- [profile](#profile)
- [storageReviews](#storagereviews)
- [storages](#storages)
- [storagesWithStaffAccess](#storageswithstaffaccess)

### agreement
Return Type | Description
-|-
[Agreement](#agreement) | 
#### Arguments
Name | Type | Description
-|-|-
id | Int! | _Represents non-fractional signed whole numeric values. Int can represent values between -(2^31) and 2^31 - 1._

### availableBoxes
Return Type | Description
-|-
[[AvailableBox](#availablebox)!]! | 
#### Arguments
Name | Type | Description
-|-|-
storageId | Int! | _Represents non-fractional signed whole numeric values. Int can represent values between -(2^31) and 2^31 - 1._

### cities
Return Type | Description
-|-
[[City](#city)!]! | 
#### Arguments
Name | Type | Description
-|-|-
region | String | 

### completedStorages
Return Type | Description
-|-
[[Storage](#storage)!]! | 
#### Arguments
Name | Type | Description
-|-|-
region | String | 

### contacts
Return Type | Description
-|-
[Contacts](#contacts)! | _Contacts_
#### Arguments
Name | Type | Description
-|-|-
region | String | 

### countryCodes
Return Type | Description
-|-
[[CountryCode](#countrycode)!]! | _Country codes_

### locksWithStaffAccess
Return Type | Description
-|-
[[BluetoothLockStaff](#bluetoothlockstaff)!]! | _Locks with staff access_
#### Arguments
Name | Type | Description
-|-|-
storageId | Int! | _Represents non-fractional signed whole numeric values. Int can represent values between -(2^31) and 2^31 - 1._

### loginByCode
> **DEPRECATED**
>
> С версии 3.0 нужно использовать signin_by_code

Return Type | Description
-|-
[User](#user) | _Login method_
#### Arguments
Name | Type | Description
-|-|-
phone | String! | _Represents textual data as UTF-8 character sequences. This type is most often used by GraphQL to represent free-form human-readable text._
code | String! | _Represents textual data as UTF-8 character sequences. This type is most often used by GraphQL to represent free-form human-readable text._

### loginByPassword
Return Type | Description
-|-
[User](#user) | _Login method_
#### Arguments
Name | Type | Description
-|-|-
email | String! | _Represents textual data as UTF-8 character sequences. This type is most often used by GraphQL to represent free-form human-readable text._
password | String! | _Represents textual data as UTF-8 character sequences. This type is most often used by GraphQL to represent free-form human-readable text._

### myBills
> **DEPRECATED**
>
> С версии 3.0 нужно использовать agreement.bills

Return Type | Description
-|-
[[Bill](#bill)!]! | 

### myBoxes
> **DEPRECATED**
>
> С версии 3.0 нужно использовать my_units

Return Type | Description
-|-
[[Box](#box)!]! | 

### myEvents
> **DEPRECATED**
>
> С версии 3.0 нужно использовать agreement.events

Return Type | Description
-|-
[[Event](#event)!]! | 
#### Arguments
Name | Type | Description
-|-|-
page | Int | 

### myStorages
> **DEPRECATED**
>
> С версии 2.0 нужно использовать my_boxes

Return Type | Description
-|-
[[Storage](#storage)!]! | 

### myUnits
Return Type | Description
-|-
[[Unit](#unit)!]! | _Units for current_user_
#### Arguments
Name | Type | Description
-|-|-
isSharedAccessVisible | Boolean | 

### offices
Return Type | Description
-|-
[[Storage](#storage)!]! | _Storages with office_

### order
Return Type | Description
-|-
[Order](#order)! | 
#### Arguments
Name | Type | Description
-|-|-
boxId | Int! | _Represents non-fractional signed whole numeric values. Int can represent values between -(2^31) and 2^31 - 1._
couponCode | String | 

### ping
Return Type | Description
-|-
String! | _Test method_
#### Arguments
Name | Type | Description
-|-|-
value | String | 

### profile
Return Type | Description
-|-
[Profile](#profile)! | _Current profile_

### storageReviews
Return Type | Description
-|-
[[StorageReview](#storagereview)!]! | 
#### Arguments
Name | Type | Description
-|-|-
id | Int! | _Represents non-fractional signed whole numeric values. Int can represent values between -(2^31) and 2^31 - 1._
page | Int | 
perPage | Int | 

### storages
> **DEPRECATED**
>
> С версии 3.0 нужно использовать offices

Return Type | Description
-|-
[[Storage](#storage)!]! | _Storages with office_

### storagesWithStaffAccess
Return Type | Description
-|-
[[Storage](#storage)!]! | _Storages with staff access_
## Mutations
- [closeAgreement](#closeagreement)
- [confirmAgreement](#confirmagreement)
- [createAgreement](#createagreement)
- [createGuestRequest](#createguestrequest)
- [createProfilePhoto](#createprofilephoto)
- [createSharedAccess](#createsharedaccess)
- [destroySharedAccess](#destroysharedaccess)
- [forceCollectEvents](#forcecollectevents)
- [saveBluetoothEvent](#savebluetoothevent)
- [sendAuthCode](#sendauthcode)
- [sendUniversalAuthCode](#senduniversalauthcode)
- [signinByCode](#signinbycode)
- [updateProfile](#updateprofile)
- [updateProfileCompany](#updateprofilecompany)
- [updateProfileCompanyEt](#updateprofilecompanyet)
- [updateProfilePersonal](#updateprofilepersonal)
- [updateProfilePersonalEt](#updateprofilepersonalet)
- [updateUser](#updateuser)
- [updateUserState](#updateuserstate)
- [webPasswordRecovery](#webpasswordrecovery)
- [webSignInByEmail](#websigninbyemail)
- [webSignInByPhone](#websigninbyphone)
- [webSignUp](#websignup)

### closeAgreement
Return Type | Description
-|-
Boolean! | _Close Agreement_
#### Arguments
Name | Type | Description
-|-|-
id | Int! | _Represents non-fractional signed whole numeric values. Int can represent values between -(2^31) and 2^31 - 1._
closeReason | String | 

### confirmAgreement
Return Type | Description
-|-
Boolean! | _Confirm Agreement_
#### Arguments
Name | Type | Description
-|-|-
id | Int! | _Represents non-fractional signed whole numeric values. Int can represent values between -(2^31) and 2^31 - 1._

### createAgreement
Return Type | Description
-|-
[OrderResult](#orderresult)! | _Create Agreement_
#### Arguments
Name | Type | Description
-|-|-
boxId | Int! | _Represents non-fractional signed whole numeric values. Int can represent values between -(2^31) and 2^31 - 1._
tariff | String! | _Represents textual data as UTF-8 character sequences. This type is most often used by GraphQL to represent free-form human-readable text._
couponCode | String | 

### createGuestRequest
Return Type | Description
-|-
[Unit](#unit) | _Create GuestRequest_
#### Arguments
Name | Type | Description
-|-|-
storageId | Int! | _Represents non-fractional signed whole numeric values. Int can represent values between -(2^31) and 2^31 - 1._
boxId | Int | 
name | String | 
phone | String | 
code | String | 
source | [GuestRequestSourceEnum](#guestrequestsourceenum) | 

### createProfilePhoto
Return Type | Description
-|-
Boolean | _Upload profile image_
#### Arguments
Name | Type | Description
-|-|-
imageData | String! | _Represents textual data as UTF-8 character sequences. This type is most often used by GraphQL to represent free-form human-readable text._

### createSharedAccess
Return Type | Description
-|-
Boolean | _Создание совместного доступа для другого пользователя_
#### Arguments
Name | Type | Description
-|-|-
name | String! | _Represents textual data as UTF-8 character sequences. This type is most often used by GraphQL to represent free-form human-readable text._
phone | String! | _Represents textual data as UTF-8 character sequences. This type is most often used by GraphQL to represent free-form human-readable text._
agreementId | Int! | _Represents non-fractional signed whole numeric values. Int can represent values between -(2^31) and 2^31 - 1._

### destroySharedAccess
Return Type | Description
-|-
Boolean | _Удаление совместного доступа для другого пользователя_
#### Arguments
Name | Type | Description
-|-|-
id | Int! | _Represents non-fractional signed whole numeric values. Int can represent values between -(2^31) and 2^31 - 1._
agreementId | Int! | _Represents non-fractional signed whole numeric values. Int can represent values between -(2^31) and 2^31 - 1._

### forceCollectEvents
Return Type | Description
-|-
Boolean! | _Force collect events for all nodes_

### saveBluetoothEvent
Return Type | Description
-|-
Boolean! | _Save unlock event from the bluetooth app_
#### Arguments
Name | Type | Description
-|-|-
lockId | Int! | _Represents non-fractional signed whole numeric values. Int can represent values between -(2^31) and 2^31 - 1._
isSuccess | Boolean! | _Represents `true` or `false` values._
agreementId | Int | 

### sendAuthCode
Return Type | Description
-|-
Boolean! | _Отправка СМС кода для существующего пользователя_
#### Arguments
Name | Type | Description
-|-|-
phone | String! | _Represents textual data as UTF-8 character sequences. This type is most often used by GraphQL to represent free-form human-readable text._

### sendUniversalAuthCode
Return Type | Description
-|-
Boolean! | _Отправка СМС кода для нового пользователя и существующего_
#### Arguments
Name | Type | Description
-|-|-
phone | String! | _Represents textual data as UTF-8 character sequences. This type is most often used by GraphQL to represent free-form human-readable text._

### signinByCode
Return Type | Description
-|-
[User](#user) | _Авторизация и создание пользователя (если его еще нет)_
#### Arguments
Name | Type | Description
-|-|-
phone | String! | _Represents textual data as UTF-8 character sequences. This type is most often used by GraphQL to represent free-form human-readable text._
code | String! | _Represents textual data as UTF-8 character sequences. This type is most often used by GraphQL to represent free-form human-readable text._

### updateProfile
Return Type | Description
-|-
[Profile](#profile)! | _Update profile_
#### Arguments
Name | Type | Description
-|-|-
surname | String | 
name | String | 
patronymic | String | 

### updateProfileCompany
Return Type | Description
-|-
[Profile](#profile) | _Update and fill profile as company (company details)_
#### Arguments
Name | Type | Description
-|-|-
extraPhone | String | 
contactName | String! | _Represents textual data as UTF-8 character sequences. This type is most often used by GraphQL to represent free-form human-readable text._
companyName | String! | _Represents textual data as UTF-8 character sequences. This type is most often used by GraphQL to represent free-form human-readable text._
address | String! | _Represents textual data as UTF-8 character sequences. This type is most often used by GraphQL to represent free-form human-readable text._
actualAddress | String | 
inn | String! | _Represents textual data as UTF-8 character sequences. This type is most often used by GraphQL to represent free-form human-readable text._
kpp | String! | _Represents textual data as UTF-8 character sequences. This type is most often used by GraphQL to represent free-form human-readable text._
bik | String! | _Represents textual data as UTF-8 character sequences. This type is most often used by GraphQL to represent free-form human-readable text._
bank | String! | _Represents textual data as UTF-8 character sequences. This type is most often used by GraphQL to represent free-form human-readable text._
checkingAccount | String! | _Represents textual data as UTF-8 character sequences. This type is most often used by GraphQL to represent free-form human-readable text._
correspondentAccount | String! | _Represents textual data as UTF-8 character sequences. This type is most often used by GraphQL to represent free-form human-readable text._
managerName | String! | _Represents textual data as UTF-8 character sequences. This type is most often used by GraphQL to represent free-form human-readable text._
managerNameGenitive | String! | _Represents textual data as UTF-8 character sequences. This type is most often used by GraphQL to represent free-form human-readable text._
managerPosition | String! | _Represents textual data as UTF-8 character sequences. This type is most often used by GraphQL to represent free-form human-readable text._

### updateProfileCompanyEt
Return Type | Description
-|-
[Profile](#profile) | _Update and fill profile as company (multiregional)_
#### Arguments
Name | Type | Description
-|-|-
extraPhone | String | 
contactName | String! | _Represents textual data as UTF-8 character sequences. This type is most often used by GraphQL to represent free-form human-readable text._
companyName | String! | _Represents textual data as UTF-8 character sequences. This type is most often used by GraphQL to represent free-form human-readable text._
address | String! | _Represents textual data as UTF-8 character sequences. This type is most often used by GraphQL to represent free-form human-readable text._
companyUid | String! | _Represents textual data as UTF-8 character sequences. This type is most often used by GraphQL to represent free-form human-readable text._

### updateProfilePersonal
Return Type | Description
-|-
[Profile](#profile) | _Update and fill profile as personal (passport data)_
#### Arguments
Name | Type | Description
-|-|-
fullName | String! | _Represents textual data as UTF-8 character sequences. This type is most often used by GraphQL to represent free-form human-readable text._
fullNumber | String! | _Represents textual data as UTF-8 character sequences. This type is most often used by GraphQL to represent free-form human-readable text._
birthday | String! | _Represents textual data as UTF-8 character sequences. This type is most often used by GraphQL to represent free-form human-readable text._
address | String! | _Represents textual data as UTF-8 character sequences. This type is most often used by GraphQL to represent free-form human-readable text._
date | String! | _Represents textual data as UTF-8 character sequences. This type is most often used by GraphQL to represent free-form human-readable text._
unitCode | String! | _Represents textual data as UTF-8 character sequences. This type is most often used by GraphQL to represent free-form human-readable text._
who | String! | _Represents textual data as UTF-8 character sequences. This type is most often used by GraphQL to represent free-form human-readable text._

### updateProfilePersonalEt
Return Type | Description
-|-
[Profile](#profile) | _Update and fill profile as personal (multiregional)_
#### Arguments
Name | Type | Description
-|-|-
fullName | String! | _Represents textual data as UTF-8 character sequences. This type is most often used by GraphQL to represent free-form human-readable text._
personalUid | String! | _Represents textual data as UTF-8 character sequences. This type is most often used by GraphQL to represent free-form human-readable text._
address | String! | _Represents textual data as UTF-8 character sequences. This type is most often used by GraphQL to represent free-form human-readable text._

### updateUser
Return Type | Description
-|-
[User](#user) | _Update user_
#### Arguments
Name | Type | Description
-|-|-
email | String | 
password | String | 

### updateUserState
Return Type | Description
-|-
Boolean! | _Update user state_
#### Arguments
Name | Type | Description
-|-|-
isActive | Boolean! | _Represents `true` or `false` values._

### webPasswordRecovery
Return Type | Description
-|-
Boolean | _Recover password from web_
#### Arguments
Name | Type | Description
-|-|-
input | [WebPasswordRecoveryInput](#webpasswordrecoveryinput)! | _Parameters for WebPasswordRecovery_

### webSignInByEmail
Return Type | Description
-|-
[User](#user) | _Sign in user by email from web_
#### Arguments
Name | Type | Description
-|-|-
input | [WebSignInByEmailInput](#websigninbyemailinput)! | _Parameters for WebSignInByEmail_

### webSignInByPhone
Return Type | Description
-|-
[User](#user) | _Sign in user by phone from web_
#### Arguments
Name | Type | Description
-|-|-
input | [WebSignInByPhoneInput](#websigninbyphoneinput)! | _Parameters for WebSignInByPhone_

### webSignUp
Return Type | Description
-|-
[WebSignUpPayload](#websignuppayload) | _Create and sign in user from web_
#### Arguments
Name | Type | Description
-|-|-
input | [WebSignUpInput](#websignupinput)! | _Parameters for WebSignUp_
## Objects
- [AccessKindEnum](#accesskindenum)
- [ActionEnum](#actionenum)
- [Admin](#admin)
- [Agreement](#agreement)
- [AgreementClosing](#agreementclosing)
- [AvailableBox](#availablebox)
- [Bill](#bill)
- [BluetoothLock](#bluetoothlock)
- [BluetoothLockStaff](#bluetoothlockstaff)
- [Box](#box)
- [Chat](#chat)
- [City](#city)
- [CompanyDetails](#companydetails)
- [Contacts](#contacts)
- [CountryCode](#countrycode)
- [Discount](#discount)
- [Error](#error)
- [Event](#event)
- [Gate](#gate)
- [GateUnit](#gateunit)
- [GuestRequestSourceEnum](#guestrequestsourceenum)
- [LockData](#lockdata)
- [Order](#order)
- [OrderResult](#orderresult)
- [Passport](#passport)
- [PrivateData](#privatedata)
- [Profile](#profile)
- [SelectOption](#selectoption)
- [SharedAccess](#sharedaccess)
- [Storage](#storage)
- [StorageReview](#storagereview)
- [Tariff](#tariff)
- [Unit](#unit)
- [UnitInterface](#unitinterface)
- [UnitKindEnum](#unitkindenum)
- [User](#user)
- [WebPasswordRecoveryInput](#webpasswordrecoveryinput)
- [WebSignInByEmailInput](#websigninbyemailinput)
- [WebSignInByPhoneInput](#websigninbyphoneinput)
- [WebSignUpInput](#websignupinput)
- [WebSignUpPayload](#websignuppayload)

### AccessKindEnum

**Values**
Name | Description
-|-
NONE | _Padlocks or Swipe cards, no remote access_
PIN | _PIN, no remote access_
FULL | _PIN + mobile app, remote access_
BLUETOOTH | _Bluetooth access_

### ActionEnum

**Values**
Name | Description
-|-
OPEN_GATE | 
OPEN_BOX | 
CLOSE_GATE | 
CLOSE_BOX | 

### Admin
_BLE LockData / PrivateData / LockData_

**Fields**
Name | Type | Description
-|-|-
adminPs | Int! | 
unlockKey | Int! | 

### Agreement
_Договор_

**Fields**
Name | Type | Description
-|-|-
amount | String! | _Месячная стоимость (формат., с валютой)_
balance | String! | _Текущий баланс стокой._
bills | [[Bill](#bill)!]! | _Список счетов_
closing | [AgreementClosing](#agreementclosing)! | _Условия закрытия договора_
creditCardNumber | String | _Последние 4 цифры привязанной карты_
dateOn | String! | _Дата договора_
debtAmount | String | _Общая сумма долга строкой (с валютой), если долга нет - NULL_
endDateOn | String | 
events | [[Event](#event)!]! | _События открытия бокса/дверей/ворот_
fullNumber | String! | _Номер договора_
html | String! | _Текст договора_
id | Int! | 
isConfirmed | Boolean! | _Пользователь подтвердил согласие с договором_
isOwner | Boolean! | _Текущий пользователь является владельцем договора_
isPaymentOverdue | Boolean! | _Платеж просрочен, уже доступ заблокирован_
isPaymentSoon | Boolean! | _Есть неоплаченные счета, баланс отрицательный, доступ еще есть_
isSharedAccessAllowed | Boolean! | _Можно ли поделиться доступом к боксу для этого договора_
lastEventTimeStr | String! | _Дата и время последнего открытия бокса/двери/ворот(в формате "%d %B в %H:%M", если нет, то "-")_
paidDays | Int! | _Сколько дней оплачено, может быть отрицательной в случае долга_
paymentEndDate | String | 
paymentOverdueDays | Int! | 
sharedAccesses | [[SharedAccess](#sharedaccess)!]! | _Список тех с кем поделились доступом_
state | String! | _"pending" - Not paid, "active" - Paid, "closing" - Paid & closing, "closed" - Complete closed_

### AgreementClosing
_Условия закрытия договора_

**Fields**
Name | Type | Description
-|-|-
closeReasons | [[SelectOption](#selectoption)!]! | _Список причин закрытия_
debt | String | _Размер долга на текущий момент (формат., с валютой)_
deposit | String | _Размер допозита, который будет возвращен (формат., с валютой)_
isCanClose | Boolean! | _Можно ли сейчас закрыть договор_
isRecalcPenalty | Boolean! | _Будет ли перерасчет стоимости аренды, за преждевременное закрытие договора_
minEndDate | String! | _Самая ранняя дата, когда можно закрыть договор без перерасчета стоимости скидки за длительность аренды_
recalcPenalty | String | _Размер доплаты, который будет необходимо вснести в случае досрочного закрытия (формат., с валютой)_

### AvailableBox
_Бокс доступный для аренды_

**Fields**
Name | Type | Description
-|-|-
capacity | String! | 
capacityText | String! | _Объём м.куб._
capacityValue | Float! | _Объём_
dimensions | String! | _Размерность: Д х Ш х В_
discountPercent | Int! | _Процент скидки_
discounts | [String!] | _Скидки_
displayDiscount | String | _Отображаемая скидка_
id | Int! | 
isEntresol | Boolean! | _Антресольный?_
levelDisplayName | String! | _Название этажа_
minPrice | String! | _Минимальная цена "от"_
minPriceWithDiscount | String! | _Минимальная цена "от" с доп.скидками_
name | String! | _Название с номером_
number | String! | _Номер_
orderUrl | String | _Ссылка на страницу заказа (web)_
size | String! | _Размер: SX, S, M, L_
space | String! | 
squareText | String! | _Площадь м.кв._
squareValue | Float! | _Площадь_
url | String | _Ссылка на страницу бокса (web)_

### Bill
_Счёт_

**Fields**
Name | Type | Description
-|-|-
alreadyPaid | String! | 
amount | String! | _Сумма счёта_
amountPayable | String! | 
contractNo | String! | 
forPeriod | String! | 
id | Int! | 
includingDeposit | String | 
invoiceDate | String! | _Дата_
invoiceDetails | String! | 
invoiceNo | String! | _Номер_
isPaid | Boolean! | _Оплачен?_
isPayable | Boolean! | _Возможно оплатить?_
isProcessing | Boolean! | 
paidDate | String | _Дата оплаты_
payUrl | String | _Ссылка на оплату_
pdfUrl | String! | _Ссылка на PDF_
period | String! | _Период оплаты_
state | String! | _Статус счёта: [pending | paid | partially_paid | rejected]_
stateText | String! | 
storageUnit | String! | 

### BluetoothLock

**Fields**
Name | Type | Description
-|-|-
id | Int! | 
lockData | [LockData](#lockdata)! | 
name | String! | 

### BluetoothLockStaff

**Fields**
Name | Type | Description
-|-|-
id | Int! | 
label | String! | 
linked | String! | 
lockData | [LockData](#lockdata)! | 
name | String! | 

### Box
_Бокс_

**Fields**
Name | Type | Description
-|-|-
accessKind | [AccessKindEnum](#accesskindenum)! | 
actionUrl | String | 
actualOpeningDelay | Int! | 
agreement | [Agreement](#agreement)! | 
bluetoothLocks | [[BluetoothLock](#bluetoothlock)!]! | 
capacity | String! | _Объём_
dimensions | String! | _Размерность: Д х Ш х В_
displaySkudPassword | String | 
doorDimensions | String | _Размеры двери бокса_
guid | String | 
id | Int! | 
isAccessEnabled | Boolean! | 
isAvailable | Boolean! | _Доступна аренда?_
isClosable | Boolean! | 
isEntresol | Boolean! | _Антресольный?_
isLit | Boolean! | _Есть освещение?_
isStatable | Boolean! | 
kind | [UnitKindEnum](#unitkindenum)! | 
level | Int! | 
levelDisplayName | String! | _Название этажа_
mainPhotoUrl | String! | _Ссылка на главную картинку_
maxWeight | String! | _Максимальная нагрузка на пол в кг._
nodeIp | String | 
number | String! | _Номера бокса_
openingDelay | Int! | 
relayId | String | 
skudPassword | String | 
skudStateText | String | 
slotNumber | Int | 
space | String! | _Площадь бокса_
stateUrl | String | 
storage | [Storage](#storage)! | _Склад_

### Chat

**Fields**
Name | Type | Description
-|-|-
label | String! | 
url | String! | 
username | String | 

### City

**Fields**
Name | Type | Description
-|-|-
id | Int! | 
name | String! | 
position | Int! | 

### CompanyDetails

**Fields**
Name | Type | Description
-|-|-
actualAddress | String | 
address | String | 
bank | String | 
bik | String | 
checkingAccount | String | 
companyName | String | 
companyUid | String | 
contactName | String | 
correspondentAccount | String | 
extraPhone | String | 
inn | String | 
kpp | String | 
managerName | String | 
managerNameGenitive | String | 
managerPosition | String | 

### Contacts

**Fields**
Name | Type | Description
-|-|-
chats | [[Chat](#chat)!]! | 
supportEmail | String! | 
supportPhone | String! | 
supportWorkTime | String! | 

### CountryCode

**Fields**
Name | Type | Description
-|-|-
imask | String! | 
label | String! | 

### Discount

**Fields**
Name | Type | Description
-|-|-
amount | Int! | 
amountStr | String! | 
amountTotal | Int! | 
amountTotalStr | String! | 
intervalMonths | Int | 
kind | String! | 
percent | Int! | 

### Error
_A readable error_

**Fields**
Name | Type | Description
-|-|-
attribute | String! | _Which input value this error came from_
message | String! | _A description of the error_

### Event

**Fields**
Name | Type | Description
-|-|-
action | [ActionEnum](#actionenum)! | 
box | [Box](#box) | 
createdAt | String! | 
gate | [Gate](#gate) | 
id | Int! | 
payload | JSON! | 

### Gate

**Fields**
Name | Type | Description
-|-|-
accessKind | [AccessKindEnum](#accesskindenum)! | 
actionUrl | String | 
actualOpeningDelay | Int! | 
bluetoothLocks | [[BluetoothLock](#bluetoothlock)!]! | 
description | String | 
displaySkudPassword | String | 
guid | String | 
id | Int! | 
isAccessEnabled | Boolean! | 
isClosable | Boolean! | 
isStatable | Boolean! | 
kind | [UnitKindEnum](#unitkindenum)! | 
name | String! | 
nodeIp | String | 
openingDelay | Int! | 
relayId | String | 
skudPassword | String | 
skudStateText | String | 
slotNumber | Int | 
stateUrl | String | 
storage | [Storage](#storage)! | 

### GateUnit

**Fields**
Name | Type | Description
-|-|-
accessKind | [AccessKindEnum](#accesskindenum)! | 
actionUrl | String | 
actualOpeningDelay | Int! | 
bluetoothLocks | [[BluetoothLock](#bluetoothlock)!]! | 
description | String | 
displaySkudPassword | String | 
guid | String | 
id | Int! | 
isAccessEnabled | Boolean! | 
isClosable | Boolean! | 
isStatable | Boolean! | 
kind | [UnitKindEnum](#unitkindenum)! | 
name | String! | 
nodeIp | String | 
openingDelay | Int! | 
relayId | String | 
skudPassword | String | 
skudStateText | String | 
slotNumber | Int | 
stateUrl | String | 

### GuestRequestSourceEnum

**Values**
Name | Description
-|-
mobile | _Mobile_
web | _Web_

### LockData
_BLE LockData_

**Fields**
Name | Type | Description
-|-|-
address | String! | 
autoLockTime | Int! | 
battery | Int! | 
lockedStatus | Int! | 
privateData | [PrivateData](#privatedata)! | 

### Order
_Ордер - содержит актуальную цену и скидки по тарифам_

**Fields**
Name | Type | Description
-|-|-
box | [Box](#box)! | 
currency | String! | 
draftAgreementHtml | String! | 
tariffs | [[Tariff](#tariff)!]! | 

### OrderResult
_Результат создания ордера на аренду бокса_

**Fields**
Name | Type | Description
-|-|-
error | String | 
isSuccess | Boolean! | 

### Passport

**Fields**
Name | Type | Description
-|-|-
address | String | 
birthday | String | 
date | String | 
number | String | 
personalUid | String | 
unitCode | String | 
who | String | 

### PrivateData
_BLE LockData / PrivateData_

**Fields**
Name | Type | Description
-|-|-
admin | [Admin](#admin)! | 
adminPasscode | String! | 
aesKey | String! | 

### Profile

**Fields**
Name | Type | Description
-|-|-
companyDetails | [CompanyDetails](#companydetails) | 
email | String! | 
fullName | String! | 
kind | String! | 
name | String! | 
passport | [Passport](#passport) | 
phone | String! | 
state | String! | 
surname | String! | 
verificationState | String! | 

### SelectOption
_Причина закрытия договора (ключ / значение)_

**Fields**
Name | Type | Description
-|-|-
key | String! | _Display name_
value | String! | _Value_

### SharedAccess

**Fields**
Name | Type | Description
-|-|-
id | Int! | 
name | String! | 
phone | String! | 

### Storage
_Склад_

**Fields**
Name | Type | Description
-|-|-
accessFromTo | String | _Время доступа на склад для клиентов (NULL - 24/7)_
address | String! | 
availableBoxesCount | Int! | _Количество боксов доступных для аренды_
availableSizes | [String!]! | _Размеры боксов, которые доступны для аренды_
boxesCount | Int! | _Всего боксов_
city | String! | _Название города где расположен склад_
companyInfo | [String!]! | _Информация о юр.лице склада_
dangerAlert | String | _Срочное/важное сообщение для клиентов склада (Markdown)_
depositPercent | Int! | _Процент депозита_
description | String! | 
discount | Int! | _Процент скидки_
displayDiscount | String | _Отображаемая скидка_
features | [String!]! | _Особенности склада_
fullAddress | String! | 
gates | [[Gate](#gate)!]! | 
id | Int! | 
isGuestAllowed | Boolean! | _Доступен гостевой визит?_
latitude | Float! | 
longitude | Float! | 
mainPhotoUrl | String! | _Ссылка на главное фото_
minPriceWithCurrency | String | _Минимальная цена бокса доступного для аренды_
myBoxes | [[Box](#box)!]! | 
name | String! | 
officeAccessFromTo | String | _Время работы офиса (NULL - 24/7), только если склад с офисом (см. Offices)_
phone | String | _Внутренний телефон склада_
rating | Float | _Рейтинг в Yandex.Maps_
reviewsCount | Int! | _Количество отзывов_
warningNote | String | _Важная информация о складе_
wifi | String | _Wi-Fi доступ_

### StorageReview
_StorageReview_

**Fields**
Name | Type | Description
-|-|-
authorAvatarUrl | String | 
authorName | String! | 
createdAtStr | String! | 
id | Int! | 
rating | Int! | 
text | String! | 

### Tariff

**Fields**
Name | Type | Description
-|-|-
couponAmount | Int! | 
couponAmountStr | String! | 
depositAmount | Int! | 
depositAmountStr | String! | 
discount | Float! | 
discounts | [[Discount](#discount)!]! | 
name | String! | 
priceMonthly | Int! | 
priceMonthlyStr | String! | 
priceWithDiscount | Int! | 
priceWithDiscountStr | String! | 
priceWoDiscount | Int! | 
priceWoDiscountStr | String! | 
totalAmount | Int! | 
totalAmountStr | String! | 

### Unit

**Fields**
Name | Type | Description
-|-|-
accessKind | [AccessKindEnum](#accesskindenum)! | 
actionUrl | String | 
actualOpeningDelay | Int! | 
agreement | [Agreement](#agreement) | 
bluetoothLocks | [[BluetoothLock](#bluetoothlock)!]! | 
boxId | Int | _ID бокса_
dimensions | String | _Размеры бокса_
displaySkudPassword | String | 
doorDimensions | String | _Размеры двери бокса_
gates | [[GateUnit](#gateunit)!]! | 
guid | String | 
id | String! | 
isAccessEnabled | Boolean! | 
isClosable | Boolean! | 
isStatable | Boolean! | 
kind | [UnitKindEnum](#unitkindenum)! | 
level | String | _Название этажа, на котором расположен бокс_
lifeTimeStr | String | _Время жизни HH:mm для гостевого визита, для договора будет NULL_
nodeIp | String | 
number | String | _Номера бокса_
openingDelay | Int! | 
relayId | String | 
skudPassword | String | 
skudStateText | String | 
slotNumber | Int | 
space | String | _Площадь бокса_
stateUrl | String | 
storage | [Storage](#storage)! | 

### UnitInterface

**Fields**
Name | Type | Description
-|-|-
accessKind | [AccessKindEnum](#accesskindenum)! | 
actionUrl | String | 
actualOpeningDelay | Int! | 
bluetoothLocks | [[BluetoothLock](#bluetoothlock)!]! | 
displaySkudPassword | String | 
guid | String | 
isAccessEnabled | Boolean! | 
isClosable | Boolean! | 
isStatable | Boolean! | 
kind | [UnitKindEnum](#unitkindenum)! | 
nodeIp | String | 
openingDelay | Int! | 
relayId | String | 
skudPassword | String | 
skudStateText | String | 
slotNumber | Int | 
stateUrl | String | 

### UnitKindEnum

**Values**
Name | Description
-|-
BOX | 
DOOR | 
BARRIER | 
GATE | 

### User
_User_

**Fields**
Name | Type | Description
-|-|-
email | String! | 
id | ID! | 
token | String | 

### WebPasswordRecoveryInput
_Autogenerated input type of WebPasswordRecovery_

**Fields**
Name | Type | Description
-|-|-
email | String! | 

### WebSignInByEmailInput
_Autogenerated input type of WebSignInByEmail_

**Fields**
Name | Type | Description
-|-|-
email | String! | 
password | String! | 

### WebSignInByPhoneInput
_Autogenerated input type of WebSignInByPhone_

**Fields**
Name | Type | Description
-|-|-
phone | String! | 
code | String! | 

### WebSignUpInput
_Autogenerated input type of WebSignUp_

**Fields**
Name | Type | Description
-|-|-
email | String! | 
password | String! | 
phone | String! | 
code | String! | 

### WebSignUpPayload
_Autogenerated return type of WebSignUp._

**Fields**
Name | Type | Description
-|-|-
errors | [[Error](#error)!] | 
user | [User](#user) | 
