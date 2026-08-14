# Code Tips & Refactoring Snippets Reference

## Meaningful Names

### Video 1: Use Intention-Revealing Names
**Principle:** Names should explain why a value exists and what it represents without requiring a comment or a trace through the code.

#### Anti-Pattern (Bad Code)
```javascript
let d;
d = getElapsedTimeInDays();
if (d > 30) {
  sendReminderEmail(d);
}
logActivity(d);
```

#### Enforced Pattern (Good Code)
```javascript
let elapsedTimeInDays = getElapsedTimeInDays();
if (elapsedTimeInDays > 30) {
  sendReminderEmail(elapsedTimeInDays);
}
logActivity(elapsedTimeInDays);
```

#### Anti-Pattern (Bad Code)
```javascript
const r = u.filter(
  x => x.s === 'a'
);
```

#### Enforced Pattern (Good Code)
```javascript
const activeUsers = users.filter(
  user => user.status === 'active'
);
```

#### Anti-Pattern (Bad Code)
```javascript
const p = b * (1 - d) + s;
```

#### Enforced Pattern (Good Code)
```javascript
const finalPrice =
  basePrice * (1 - discount) + shippingCost;
```

### Video 2: Avoid Disinformation
**Principle:** Names must accurately describe the value they hold and must not create false expectations through misleading words, near-duplicates, or ambiguous characters.

#### Anti-Pattern (Bad Code)
```javascript
let accountList = {
  "user1": {name: "John", ...},
  "user2": {name: "Doe", ...},
};
```

#### Enforced Pattern (Good Code)
```javascript
let accounts = {
  "user1": {name: "John", ...},
  "user2": {name: "Doe", ...},
};
```

#### Anti-Pattern (Bad Code)
```javascript
let isComplete = "pending";
let userCount = {total: 42};
let settingMap = true;
```

#### Enforced Pattern (Good Code)
```javascript
let status = "pending";
let userStats = {total: 42};
let debugEnabled = true;
```

### Video 3: Make Meaningful Distinctions
**Principle:** Different names should represent genuinely different behavior or responsibility, not meaningless variations or generic suffixes.

#### Anti-Pattern (Bad Code)
```javascript
function getUser() {...}
function getUserInfo() {...}
function getUserData() {...}
```

#### Enforced Pattern (Good Code)
```javascript
function getUserProfile() {...}
function getUserPreferences() {...}
function getUserPermissions() {...}
```

#### Anti-Pattern (Bad Code)
```javascript
function filterAndMap(data1, data2, data3) {
  const result = data1.filter(data2).map(data3);
  return result;
}
```

#### Enforced Pattern (Good Code)
```javascript
function filterAndMap(array, condition, transformation) {
  const result = array.filter(condition).map(transformation);
  return result;
}
```

### Video 4: Use Pronounceable Names
**Principle:** Names should sound like natural language so developers can discuss them in reviews, documentation, and everyday conversation.

#### Anti-Pattern (Bad Code)
```javascript
let genymdhms = new Date();
let prcsrr = new Processor();
let usrRcrds = [];
let dtaRcrd = fetchData();
```

#### Enforced Pattern (Good Code)
```javascript
let generationTimestamp = new Date();
let processor = new Processor();
let userRecords = [];
let dataRecord = fetchData();
```

### Video 5: Use Searchable Names
**Principle:** The name should be long and specific enough to search for when its scope is larger than a short local context.

#### Anti-Pattern (Bad Code)
```javascript
for (let e = 0; e < 7; e++) {
  total += (data[e] * 4) / 5;
}
```

#### Enforced Pattern (Good Code)
```javascript
for (let j = 0; j < NUMBER_OF_TASKS; j++) {
  let taskDays = taskEstimate[j] * DAYS_PER_IDEAL_DAY;
  let taskWeeks = taskDays / WORK_DAYS_PER_WEEK;
  sum += taskWeeks;
}
```

### Video 6: Avoid Encodings
**Principle:** Do not encode type information into names when the language, compiler, or IDE already exposes the type.

#### Anti-Pattern (Bad Code)
```typescript
let strFirstName: string;
let iAge: number;
let bIsLoggedIn: boolean;
let fAccountBalance: number;
```

#### Enforced Pattern (Good Code)
```typescript
let firstName: string;
let age: number;
let isLoggedIn: boolean;
let accountBalance: number;
```

### Video 7: Avoid Mental Mapping
**Principle:** Readers should not have to translate cryptic abbreviations or single-letter variables into domain concepts before understanding the logic.

#### Anti-Pattern (Bad Code)
```javascript
function calculateTotal(p, t, q) {
  return (p + t) * q;
}
```

#### Enforced Pattern (Good Code)
```javascript
function calculateTotal(price, tax, quantity) {
  return (price + tax) * quantity;
}
```

### Video 8: Small Functions
**Principle:** Keep functions small by moving low-level details behind names that explain the operation being performed.

#### Anti-Pattern (Bad Code)
```javascript
async function uploadFile(file, userId) {
  const filePath = buildFilePath(file, userId);

  if (file.size > MAX_SINGLE_UPLOAD_SIZE) {
    const uploadId = await Storage.initMultipartUpload(filePath);
    const totalChunks = Math.ceil(file.size / CHUNK_SIZE);

    for (let i = 0; i < totalChunks; i++) {
      const start = i * CHUNK_SIZE;
      const end = Math.min(start + CHUNK_SIZE, file.size);
      const chunk = file.slice(start, end);
      await Storage.uploadPart(uploadId, i, chunk);
    }

    await Storage.completeMultipartUpload(uploadId);
    return { path: filePath, method: "multipart" };
  }

  await Storage.upload(filePath, file.buffer);
  return { path: filePath, method: "single" };
}
```

#### Enforced Pattern (Good Code)
```javascript
async function uploadFile(file, userId) {
  const filePath = buildFilePath(file, userId);

  if (file.size > MAX_SINGLE_UPLOAD_SIZE) {
    return uploadFileInParts(file, filePath);
  }

  return uploadFileAsSinglePart(file, filePath);
}
```

### Video 9: Do One Thing
**Principle:** A function should have one responsibility and should not contain a separately nameable concept that can be extracted without merely restating its implementation.

#### Anti-Pattern (Bad Code)
```javascript
function processOrder(order) {
  const inventory = database.getItems(order.itemIds);
  for (const item of inventory) {
    if (item.stock < order.qty) {
      throw new Error("Out of stock");
    }
  }

  const finalBill = calculateTotalBill(order);

  try {
    Stripe.charges.create({
      amount: finalBill * 100,
      source: order.paymentToken
    });
  } catch (e) {
    throw new Error("Payment Failed");
  }

  Mailer.send({
    to: order.customerEmail,
    subject: "Order Confirmed",
    body: `Your total: ${finalBill}`
  });
}
```

#### Enforced Pattern (Good Code)
```javascript
function processOrder(order) {
  validateStockAvailability(order);
  const finalBill = calculateTotalBill(order);
  executeStripeCharge(order.customer.token, finalBill);
  notifyWarehouse(order);
}
```

### Video 10: Levels of Abstraction
**Principle:** Functions should tell a top-down story, with each function operating at one level of abstraction and delegating implementation details to lower-level functions.

#### Anti-Pattern (Bad Code)
```javascript
function processOrder(order) {
  const inventory = database.getItems(order.itemIds);
  for (const item of inventory) {
    if (item.stock < order.qty) {
      throw new Error("Out of stock");
    }
  }

  let subtotal = 0;
  for (const item of order.items) {
    const discount = applyDiscount(item.price);
    const tax = calculateTax(subtotal - discount);
    subtotal = item.price + tax;
  }

  try {
    Stripe.charges.create({
      amount: finalBill * 100,
      source: order.paymentToken
    });
  } catch (e) {
    throw new Error("Payment Failed");
  }

  Mailer.send({
    to: order.customerEmail,
    subject: "Order Confirmed",
    body: `Your total: ${finalBill}`
  });
}
```

#### Enforced Pattern (Good Code)
```javascript
function processOrder(order) {
  validateStockAvailability(order);
  const finalBill = calculateTotalBill(order);
  executeStripeCharge(order.customer.token, finalBill);
  notifyWarehouse(order);
}
```

## Switch Statements

### Video 1: Handling Switch Statements with Polymorphism
**Principle:** Replace repeated type switches with polymorphic objects so the type-specific behavior lives with the type that owns it.

#### Anti-Pattern (Bad Code)
```javascript
function calculatePay(employee) {
  switch (employee.type) {
    case 'fullTime':
      return employee.salary / 12;
    case 'partTime':
      return employee.hours * employee.rate;
    case 'contractor':
      return employee.hours * employee.contractRate;
  }
}
```

#### Enforced Pattern (Good Code)
```typescript
class EmployeeFactory {
  // The switch lives here—and ONLY here
  create(type, data): Employee {
    switch (type) {
      case 'fullTime':
        return new FullTimeEmployee(data);
      case 'partTime':
        return new PartTimeEmployee(data);
      case 'contractor':
        return new Contractor(data);
    }
  }
}

const contractor = factory.create('contractor', data);
contractor.calculatePay();
contractor.getBenefits();
contractor.getSchedule();
```

### Video 2: Keep Argument Lists Short
**Principle:** Zero arguments is ideal, one is clear, two can be acceptable, and three or more usually signal that related values should become an object.

#### Anti-Pattern (Bad Code)
```javascript
saveUser(name, email, age, city, isPremium)
```

#### Enforced Pattern (Good Code)
```javascript
saveUser(user)
```

### Video 3: Avoid Flag and Output Arguments
**Principle:** Boolean flags hide alternate responsibilities, while output arguments violate the normal expectation that data flows in through parameters and out through return values.

#### Anti-Pattern (Bad Code)
```javascript
createUser(true)
findMax(numbers, result)
```

#### Enforced Pattern (Good Code)
```javascript
createAdminAccount()

function findMax(numbers) {
  return Math.max(numbers)
}
```

### Video 4: Make Arguments Clear
**Principle:** Related values can be grouped, but unrelated pairs and ambiguous triads should be made explicit through ownership, names, and a predictable ordering.

#### Anti-Pattern (Bad Code)
```javascript
sendEmail(message, smtp)
```

#### Enforced Pattern (Good Code)
```javascript
smtp.sendEmail(message)
```

### Video 5: Remove Side Effects
**Principle:** A function should do what its name promises; a check should not silently initialize a session or mutate object state.

#### Anti-Pattern (Bad Code)
```javascript
function checkPassword(password) {
  if (password === storedPassword) {
    Session.initialize();
    return true;
  }
  return false;
}
```

#### Enforced Pattern (Good Code)
```javascript
function checkPassword(password) {
  if (password === storedPassword) {
    return true;
  }
  return false;
}

if (checkPassword(password)) {
  initializeSession();
}
```

### Video 6: Separate Commands and Queries
**Principle:** Commands change state and queries return answers; combining them makes a call impossible to reason about safely.

#### Anti-Pattern (Bad Code)
```javascript
function setAndCheckIfExists(attribute, value) {
  const existed = data[attribute] !== undefined;
  data[attribute] = value;
  return existed;
}
```

#### Enforced Pattern (Good Code)
```javascript
if (!attributeExists("role")) {
  setAttribute("role", "admin");
}
```

### Video 7: Prefer Exceptions to Error Codes
**Principle:** Exceptions keep the normal path flat and localize error handling instead of forcing every caller through nested status checks and shared error enums.

#### Anti-Pattern (Bad Code)
```javascript
if (createAccount(userData) == ErrorCode.OK) {
  if (createProfile(userData) == ErrorCode.OK) {
    if (sendWelcomeEmail(userData.email) == ErrorCode.OK) {
      return ErrorCode.OK;
    } else {
      return ErrorCode.EMAIL_FAILED;
    }
  } else {
    return ErrorCode.PROFILE_FAILED;
  }
} else {
  return ErrorCode.ACCOUNT_FAILED;
}
```

#### Enforced Pattern (Good Code)
```javascript
function registerUser(userData) {
  try {
    performRegistration(userData);
  } catch (error) {
    showError(error.message);
  }
}

function performRegistration(userData) {
  createAccount(userData);
  createProfile(userData);
  sendWelcomeEmail(userData.email);
  redirectToDashboard();
}
```

### Video 8: Do Not Repeat Yourself
**Principle:** Each piece of knowledge should have one authoritative representation so a change such as a timeout is made in one place.

#### Anti-Pattern (Bad Code)
```javascript
async function getUsers() {
  const res = await fetch('/api/users');
  if (!res.ok) throw new Error();
  return res.json();
}

async function getPosts() {
  const res = await fetch('/api/posts');
  if (!res.ok) throw new Error();
  return res.json();
}
```

#### Enforced Pattern (Good Code)
```javascript
async function fetchData(endpoint, timeout = 5000) {
  const res = await fetch(endpoint, { timeout });
  if (!res.ok) throw new Error('Failed');
  return res.json();
}

async function getUsers() {
  return fetchData('/api/users');
}

async function getPosts() {
  return fetchData('/api/posts');
}
```

### Video 9: Refactor in Small Iterations
**Principle:** Clean code is usually rewritten into shape through small, test-backed refactorings rather than written perfectly on the first attempt.

#### Anti-Pattern (Bad Code)
```javascript
<!-- Snippet visual missing from keyframe assets -->
```

#### Enforced Pattern (Good Code)
```javascript
<!-- Snippet visual missing from keyframe assets -->
```

## Commenting

### Video 1: Commenting Overview
**Principle:** Comments can become stale and misleading as code changes, so they should exist only when they communicate something the code cannot.

#### Anti-Pattern (Bad Code)
```javascript
<!-- Snippet visual missing from keyframe assets -->
```

#### Enforced Pattern (Good Code)
```javascript
<!-- Snippet visual missing from keyframe assets -->
```

### Video 2: Explain Non-Obvious Constraints
**Principle:** Useful comments preserve business constraints, warnings, or non-intuitive rules that cannot be inferred from the implementation alone.

#### Anti-Pattern (Bad Code)
```javascript
expect(a.compareTo(b)).toBe(-1);
```

#### Enforced Pattern (Good Code)
```javascript
// a < b
expect(a.compareTo(b)).toBe(-1);
```

### Video 3: Use Warnings and TODOs
**Principle:** Warnings should explain a real operational constraint, and TODOs should record a specific reason the work cannot yet be completed.

#### Anti-Pattern (Bad Code)
```javascript
function testWithReallyBigFile() {
  writeLinesToFile(10_000_000);
}
```

#### Enforced Pattern (Good Code)
```javascript
// WARNING: Takes too long to run.
// Skip during test cycles.
function testWithReallyBigFile() {
  writeLinesToFile(10_000_000);
}
```

### Video 4: Document Public Code
**Principle:** Public APIs need documentation describing purpose, inputs, outputs, failures, and usage; legal headers should use standard licenses.

#### Anti-Pattern (Bad Code)
```javascript
function fetchUser(id) {
  // ... implementation
}
```

#### Enforced Pattern (Good Code)
```javascript
/**
 * Fetches a user by identifier.
 * @param {string} id - The user identifier.
 * @returns {Promise<User>} The requested user.
 */
function fetchUser(id) {
  // ... implementation
}
```

### Video 5: Remove Redundant Comments
**Principle:** A comment that repeats the code adds scanning and maintenance cost without adding understanding.

#### Anti-Pattern (Bad Code)
```javascript
// if there are no items in the cart,
// return early.
if (cart.items.length === 0) {
  return;
}
```

#### Enforced Pattern (Good Code)
```javascript
if (cart.items.length === 0) {
  return;
}
```

### Video 6: Avoid Misleading Comments
**Principle:** Comments must be specific, obvious, and local; otherwise they create false confidence or force the reader to guess what they mean.

#### Anti-Pattern (Bad Code)
```javascript
// Returns the discount
// percentage for premium users
function getDiscount(user) {
  if (user.isPremium) return 20;
  return 5;
}
```

#### Enforced Pattern (Good Code)
```javascript
function getDiscount(user) {
  if (user.isPremium) return 20;
  return 5;
}
```

### Video 7: Remove Commented-Out Code
**Principle:** Deleted code belongs in version control, not in the active source file alongside code that actually runs.

#### Anti-Pattern (Bad Code)
```javascript
// function getUserInfo() { ... }
// const oldValue = getLegacyValue();
function getUser(id) {
  return loadUser(id);
}
```

#### Enforced Pattern (Good Code)
```javascript
function getUser(id) {
  return loadUser(id);
}
```

### Video 8: Remove Structural Apology Comments
**Principle:** Closing-brace comments and position markers usually indicate that the function or file needs structural refactoring rather than more labels.

#### Anti-Pattern (Bad Code)
```javascript
function generateReport(data) {
  if (data.length > 0) {
    for (let i = 0; i < data.length; i++) {
      try {
        if (data[i].isValid()) {
          while (data[i].hasNext()) {
            process(data[i]);
          } // end while hasNext
        } // end if isValid
      } catch (e) {
        // error handling ...
      } // end for
    } // end if data
  } // end generateReport
}
```

#### Enforced Pattern (Good Code)
```javascript
function generateReport(data) {
  const validItems = filterValid(data);
  const results = processItems(validItems);
  return buildReport(results);
}
```

### Video 9: Write Clear, Relevant Comments
**Principle:** Replace vague comments with actionable TODOs, remove irrelevant history, and use plain text that remains readable in the editor.

#### Anti-Pattern (Bad Code)
```javascript
// R.J. said this might cause a race condition if the server is slow.
// I tried to fix it but not sure if it works for the edge case.
// load the user data
if (user.id) {
  loadData(user.id);
}
```

#### Enforced Pattern (Good Code)
```javascript
// TODO: Add a timeout check here.
// Currently, if the server response is slow, the UI freezes.
if (user.id) {
  loadData(user.id);
}
```

## Formatting

### Video 1: Read Code Like a Newspaper
**Principle:** Put the highest-level function first, define supporting functions below their callers, and group conceptually related helpers together.

#### Anti-Pattern (Bad Code)
```javascript
function fetchUserData(userId) {
  // ... get data from the database
}

function saveReport(reportText) {
  // ... save to the database
}

function processUserReport(userId) {
  let rawData = fetchUserData(userId);
  let report = buildReport(rawData);
  saveReport(report);
}

function buildReport(data) {
  let cleanDate = formatDate(data.date);
  let cleanScore = formatScore(data.score);
  return data.name + ": " + cleanDate
    + " " + cleanScore;
}
```

#### Enforced Pattern (Good Code)
```javascript
function processUserReport(userId) {
  let rawData = fetchUserData(userId);
  let report = buildReport(rawData);
  saveReport(report);
}

function fetchUserData(userId) {
  // ... get data from the database
}

function buildReport(data) {
  let cleanDate = formatDate(data.date);
  let cleanScore = formatScore(data.score);
  return data.name + ": " + cleanDate
    + " " + cleanScore;
}

function saveReport(reportText) {
  // ... save to the database
}
```

### Video 2: Use Vertical Spacing and Indentation
**Principle:** Blank lines separate concepts, dense lines keep related operations together, and indentation makes scope visible at a glance.

#### Anti-Pattern (Bad Code)
```typescript
import { User } from '../models';
import { CacheConfig } from '../config';
class UserProfileService {
private user: User;
private cache: Map<string, string>;
private isInitialized: boolean;
constructor(user: User) {...}
generateUserProfileBadge() {...}
getDisplayName() {...}
updateUsername(newUsername: string) {...}
deleteProfile() {...}
}
```

#### Enforced Pattern (Good Code)
```typescript
import { User } from '../models';
import { CacheConfig } from '../config';

class UserProfileService {
  private user: User;
  private cache: Map<string, string>;
  private isInitialized: boolean;

  constructor(user: User) {...}

  generateUserProfileBadge() {...}

  getDisplayName() {...}

  updateUsername(newUsername: string) {...}

  deleteProfile() {...}
}
```

### Video 3: Declare Variables Near Their Use
**Principle:** Local variables should be introduced where they are needed, while shared class properties should stay in the class’s designated field area.

#### Anti-Pattern (Bad Code)
```javascript
let skippedLog;
let report;

// ... other processing

if (hasDuplicates) {
  skippedLog = buildDuplicateReport();
  notifyAdmin(skippedLog);
}

// ... more processing

report = buildImportReport(validated, rows);
archiveReport(report);
return report;
```

#### Enforced Pattern (Good Code)
```javascript
// ... other processing

if (hasDuplicates) {
  const skippedLog = buildDuplicateReport();
  notifyAdmin(skippedLog);
}

// ... more processing

const report = buildImportReport(validated, rows);
archiveReport(report);
return report;
```

## Objects and Data

### Video 1: Expose Behavior, Not Structure
**Principle:** Abstraction should hide representation and expose what callers can do, including access policies and meaningful behavior.

#### Anti-Pattern (Bad Code)
```java
public class Point {
  public double x;
  public double y;
}
```

#### Enforced Pattern (Good Code)
```java
public interface Point {
  double getX();
  double getY();
  void setCartesian(double x, double y);
  double getR();
  double getTheta();
  void setPolar(double r, double theta);
}
```

#### Anti-Pattern (Bad Code)
```java
public interface Vehicle {
  public double getFuelTankCapacityInGallons();
  public double getGallonsOfGasoline();
}
```

#### Enforced Pattern (Good Code)
```java
public interface Vehicle {
  double getPercentFuelRemaining();
}
```

### Video 2: Choose Data Structures or Objects
**Principle:** Procedural designs make adding operations easy, while object-oriented designs make adding types easy; choose based on the change most likely to come next.

#### Anti-Pattern (Bad Code)
```java
class Square {
  public double side;
}

class Rectangle {
  public double height;
  public double width;
}

class Circle {
  public double radius;
}

class Geometry {
  double area(Object s) {
    if (s instanceof Square)
      return s.side * s.side;
    if (s instanceof Rectangle)
      return s.height * s.width;
    if (s instanceof Circle)
      return PI * s.radius * s.radius;
  }
}
```

#### Enforced Pattern (Good Code)
```java
class Square implements Shape {
  private double side;

  double area() {
    return side * side;
  }
}

class Rectangle implements Shape {
  private double height;
  private double width;

  double area() {
    return height * width;
  }
}

class Circle implements Shape {
  private double radius;

  double area() {
    return PI * radius * radius;
  }
}
```

### Video 3: Follow the Law of Demeter
**Principle:** Talk to immediate collaborators and tell an object what you need instead of reaching through a chain of returned objects.

#### Anti-Pattern (Bad Code)
```javascript
let outputDir =
  ctxt.getOptions()
    .getScratchDir()
    .getAbsolutePath();
```

#### Enforced Pattern (Good Code)
```javascript
let outputDir =
  ctxt.getAbsolutePathForScratchDirectoryOption();
```

### Video 4: Keep Objects and Data Structures Pure
**Principle:** Objects hide data and expose behavior, while data structures expose data and avoid behavior; hybrid classes lose the advantages of both designs.

#### Anti-Pattern (Bad Code)
```java
class Product {
  private String name;
  private double price;

  String getName() { return name; }
  double getPrice() { return price; }
  void setPrice(double p) { price = p; }

  double applyDiscount(double pct) {
    return price * (1 - pct / 100);
  }
}
```

#### Enforced Pattern (Good Code)
```java
class Product extends ActiveRecord {
  private String name;
  private double price;

  void save() { ... }
  void delete() { ... }
}

class ProductPricing {
  double applyDiscount(Product p, double pct) {
    return p.getPrice() * (1 - pct / 100);
  }
}
```

## Error Handling

### Video 1: Prefer Exceptions Over Return Codes
**Principle:** Keep the algorithm readable by moving failure handling out of every normal-processing step and into one exception boundary.

#### Anti-Pattern (Bad Code)
```javascript
function sendMessage(msg) {
  const sender = verifySession(msg.token);
  if (sender === null) {
    return "expired";
  }
  const channel = resolveChannel(msg.to);
  if (channel.active === false) {
    return "closed";
  }
  const content = moderate(msg.text);
  if (content.ok) {
    broadcast(channel, sender, content);
    return "sent";
  } else {
    return "blocked";
  }
}
```

#### Enforced Pattern (Good Code)
```javascript
function sendMessage(msg) {
  try {
    deliverMessage(msg);
  } catch (error) {
    notifySender(msg.token, error);
  }
}

function deliverMessage(msg) {
  const sender = verifySession(msg.token);
  const channel = resolveChannel(msg.to);
  const content = moderate(msg.text);
  broadcast(channel, sender, content);
}
```

### Video 2: Write the Try-Catch Contract First
**Principle:** Define the exception contract and failure test before filling in the implementation so callers know exactly what the function can throw.

#### Anti-Pattern (Bad Code)
```javascript
function withdraw(accountId, amount) {
  const account = await db.load(accountId);
  account.assertActive();
  account.debit(amount);
  await db.save(account);
}
```

#### Enforced Pattern (Good Code)
```javascript
function withdraw(accountId, amount) {
  try {
    const account = await db.load(accountId);
    account.assertActive();
    account.debit(amount);
    await db.save(account);
  } catch (e) {
    throw new TransactionFailed(e);
  } finally {
    await lock.release(accountId);
  }
}
```

### Video 3: Wrap Third-Party APIs
**Principle:** Translate library-specific exception types at a wrapper boundary so the rest of the application depends on exceptions chosen by the application.

#### Anti-Pattern (Bad Code)
```java
S3Client s3 = new S3Client(region);
try {
  s3.getObject(key);
} catch (NoSuchKeyException e) {
  notifyOps(e);
} catch (SdkClientException e) {
  notifyOps(e);
} catch (S3Exception e) {
  notifyOps(e);
}
```

#### Enforced Pattern (Good Code)
```java
class ObjectStore {
  S3Client s3;

  File fetch(String key) {
    try {
      return s3.getObject(key);
    } catch (NoSuchKeyException e) {
      throw new StorageFailure(e);
    } catch (SdkClientException e) {
      throw new StorageFailure(e);
    } catch (S3Exception e) {
      throw new StorageFailure(e);
    }
  }
}

ObjectStore store = new ObjectStore();
try {
  store.fetch(key);
} catch (StorageFailure e) {
  notifyOps(e);
  logger.log("Fetch failed", e);
}
```

### Video 4: Use Special Cases for Expected Branches
**Principle:** Do not use exceptions for normal alternatives such as a missing regional tax rule; return a default object with the same interface instead.

#### Anti-Pattern (Bad Code)
```java
TaxRule rule;
double tax;
try {
  rule = taxRules.findFor(region);
  tax = rule.calculate(subtotal);
} catch (NoRuleFound e) {
  tax = subtotal * STANDARD_RATE;
}
total += tax;
```

#### Enforced Pattern (Good Code)
```java
TaxRule findFor(String region) {
  if (rules.containsKey(region)) {
    return rules.get(region);
  }
  return new StandardTaxRule();
}

class StandardTaxRule implements TaxRule {
  public double calculate(double subtotal) {
    return subtotal * STANDARD_RATE;
  }
}
```

### Video 5: Return Empty Values Instead of Null
**Principle:** Use sensible empty values such as an empty list or zero where absence is normal, and reserve exceptions for failures that should not be silently ignored.

#### Anti-Pattern (Bad Code)
```java
List<Order> orders = customer.getOrders();
if (orders != null) {
  for (Order o : orders) {
    Double discount = o.getDiscount();
    if (discount != null) {
      total += o.getAmount() - discount;
    }
  }
}
```

#### Enforced Pattern (Good Code)
```java
List<Order> orders = customer.getOrders();
for (Order o : orders) {
  Double discount = o.getDiscount();
  total += o.getAmount() - discount;
}

public List<Order> getOrders() {
  if (orders == null) return List.of();
  return orders;
}

public Double getDiscount() {
  if (discount == null) return 0.0;
  return discount;
}
```

## Boundaries

### Video 1: Wrap Third-Party Libraries at the Boundary
**Principle:** Keep third-party library details behind a small wrapper so the rest of the codebase depends on an API the application owns.

#### Anti-Pattern (Bad Code)
```typescript
import Stripe from 'stripe';

const stripe = new Stripe(
  process.env.STRIPE_KEY,
);

export async function checkout(
  order: Order,
) {
  const charge =
    await stripe.charges.create({
      amount: order.total,
      currency: 'usd',
      source: order.card,
    });
  order.markPaid(charge.id);
}
```

#### Enforced Pattern (Good Code)
```typescript
export class Payments {
  private stripe = new Stripe(
    process.env.STRIPE_KEY,
  );

  async charge(
    order: Order,
  ): Promise<string> {
    const intent = await this.stripe
      .paymentIntents.create({
        amount: order.total,
        currency: 'usd',
        payment_method: order.card,
        confirm: true,
      });
    return intent.id;
  }

  async refund(
    paymentId: string,
  ): Promise<void> {
    await this.stripe.refunds.create({
      payment_intent_id: paymentId,
    });
  }
}

import { Payments }
from './payments';

const payments = new Payments();

export async function checkout(
  order: Order,
) {
  const id =
    await payments.charge(order);
  order.markPaid(id);
}
```

### Video 2: The Adapter Pattern
**Principle:** Define the interface your application needs, test against it before the provider exists, and use one adapter to translate that interface to the provider's API.

#### Anti-Pattern (Bad Code)
```typescript
export async function checkout(
  cart: Cart,
  card: Card,
) {
  const total = priceOf(cart);
  // TODO: charge the card
  return confirmOrder(cart);
}
```

#### Enforced Pattern (Good Code)
```typescript
export interface Payments {
  charge(
    amount: number,
    card: Card,
  ): Promise<Receipt>;
}

import { Payments }
from './payments';

export async function checkout(
  cart: Cart,
  card: Card,
  payments: Payments,
) {
  const total = priceOf(cart);
  await payments.charge(total, card);
  return confirmOrder(cart);
}
```

#### Anti-Pattern (Bad Code)
```typescript
export class PaylinkClient {
  createCharge(params: {
    amountInCents: number;
    currency: string;
    token: string;
  }): Promise<PaylinkCharge>;
}
```

#### Enforced Pattern (Good Code)
```typescript
class PaylinkAdapter
  implements Payments {
  paylink = new PaylinkClient();

  async charge(
    amount: number,
    card: Card,
  ) {
    const result = await paylink
      .createCharge({
        amountInCents:
          Math.round(amount * 100),
        currency: 'usd',
        token: card.token,
      });
    return toReceipt(result);
  }
}
```

#### Anti-Pattern (Bad Code)
```typescript
export async function checkout(
  cart: Cart,
  card: Card,
) {
  const total = priceOf(cart);
  // TODO: charge the card
  return confirmOrder(cart);
}
```

#### Enforced Pattern (Good Code)
```typescript
class FakeGateway
  implements Payments {
  async charge(
    amount: number,
    card: Card,
  ) {
    return approvedReceipt();
  }
}

it('charges the card', async () => {
  const order = await checkout(
    cart, card, new FakeGateway(),
  );
  expect(order.paid).toBe(true);
});
```
