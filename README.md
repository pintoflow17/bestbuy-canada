# BestBuy Canada API Documentation

## Getting Started

To use the BestBuy Canada API, you'll need to:
1. Sign up for a RapidAPI account
2. Subscribe to the [BestBuy Canada API](https://rapidapi.com/belchiorarkad-FqvHs2EDOtP/api/bestbuy-canada)
3. Obtain your API key from RapidAPI
4. Include your API key in the `X-RapidAPI-Key` header with each request

Base URL: `https://bestbuy-canada.p.rapidapi.com`

Default response language is English (en-CA), but French (fr-CA) is also supported for most endpoints.

## Search Endpoints

### Product Search
```
GET /search
```
Search for products across BestBuy Canada's catalog.

Parameters:
- `query` (required): Search term
- `page` (optional, default: 1): Page number
- `perPage` (optional, default: 20): Results per page
- `lang` (optional, default: en-CA): Language (en-CA or fr-CA)

## Product Endpoints

### Products by Category
```
GET /product/bycategory
```
Get products within a specific category.

Parameters:
- `categoryId` (required): Category identifier
- `page` (optional, default: 1): Page number
- `perPage` (optional, default: 20): Results per page
- `lang` (optional, default: en-CA): Language

### Product Reviews
```
GET /product/review
```
Get reviews for a specific product.

Parameters:
- `productId` (required): Product identifier
- `page` (optional, default: 1): Page number
- `perPage` (optional, default: 20): Results per page
- `lang` (optional, default: en-CA): Language

### Product Review Summary
```
GET /product/review/summary
```
Get aggregated review statistics for a product.

Parameters:
- `productId` (required): Product identifier

### Product Offers
```
GET /product/offers
```
Get current offers for a product.

Parameters:
- `productId` (required): Product identifier
- `postalCode` (optional, default: M5A): Postal code for location-specific offers

### Product Availability
```
GET /product/availability
```
Check product availability in stores.

Parameters:
- `skus` (required): Product SKUs (comma-separated for multiple)
- `lang` (optional, default: en-CA): Language
- `postalCode` (optional, default: M5G2C3): Postal code for store lookup

### Product Description
```
GET /product/description
```
Get detailed product description.

Parameters:
- `productId` (required): Product identifier
- `lang` (optional, default: en-CA): Language

### Product ID Lookup
```
GET /product/id
```
Get product ID from product URL.

Parameters:
- `productUrl` (required): BestBuy product URL

### Product Media
```
GET /product/media
```
Get product images and media assets.

Parameters:
- `productId` (required): Product identifier
- `lang` (optional, default: en-CA): Language

### Product Conditions
```
GET /product/conditions
```
Get available product conditions (new, refurbished, etc.).

Parameters:
- `productId` (required): Product identifier
- `lang` (optional, default: en-CA): Language

### Product Special Offers
```
GET /product/special-offers
```
Get special offers and promotions for a product.

Parameters:
- `productId` (required): Product identifier
- `lang` (optional, default: en-CA): Language

## Category Endpoints

### Category Description
```
GET /category/description
```
Get detailed category description.

Parameters:
- `categoryId` (required): Category identifier
- `lang` (optional, default: en-CA): Language

### Category List
```
GET /category/list
```
Get list of all available categories.

Parameters:
- `lang` (optional, default: en-CA): Language

## Example Usage

```javascript
const axios = require('axios');

const options = {
  method: 'GET',
  url: 'https://bestbuy-canada.p.rapidapi.com/search',
  params: {
    query: 'iphone',
    page: '1',
    perPage: '20',
    lang: 'en-CA'
  },
  headers: {
    'X-RapidAPI-Key': 'YOUR_RAPIDAPI_KEY',
    'X-RapidAPI-Host': 'bestbuy-canada.p.rapidapi.com'
  }
};

try {
  const response = await axios.request(options);
  console.log(response.data);
} catch (error) {
  console.error(error);
}
```

## Error Handling

The API returns standard HTTP status codes:
- 200: Success
- 400: Bad Request (missing or invalid parameters)
- 401: Unauthorized (invalid API key)
- 429: Too Many Requests (rate limit exceeded)
- 500: Internal Server Error

Error responses include an error message and status code in the response body.

---

### BestBuy: Your Go-To Retailer for Electronics and More

BestBuy is a leading multinational retailer specializing in consumer electronics, home appliances, entertainment products, and services. Founded in 1966 and headquartered in Richfield, Minnesota, BestBuy has established itself as a trusted name for high-quality products and exceptional customer service. With both an extensive online platform and physical store presence, BestBuy caters to millions of customers seeking reliable solutions for their tech needs.

---

### A Wide Range of Products

BestBuy offers an impressive selection of products to meet diverse needs, including:

#### 1. **Consumer Electronics**
   - Smartphones from top brands like Apple, Samsung, and Google.
   - Tablets, eReaders, and accessories.
   - Laptops, desktops, and gaming PCs from renowned manufacturers.

#### 2. **Home Appliances**
   - Smart refrigerators, ovens, and dishwashers.
   - Washers, dryers, and vacuum cleaners.
   - Air conditioners and purifiers.

#### 3. **Entertainment**
   - 4K UHD TVs, OLED displays, and projectors.
   - Sound systems, headphones, and smart speakers.
   - Gaming consoles like PlayStation, Xbox, and Nintendo Switch.

#### 4. **Smart Home Solutions**
   - Smart lighting, thermostats, and security cameras.
   - Home automation systems compatible with Alexa, Google Assistant, and Siri.

#### 5. **Accessories and Peripherals**
   - Chargers, cases, and cables.
   - Keyboards, mice, and monitors for productivity.
   - Wearable tech like fitness trackers and smartwatches.

---

### Why Choose BestBuy?

#### 1. **Competitive Pricing**
BestBuy is known for offering attractive prices, frequent sales, and price-matching policies, ensuring customers get the best value for their money.

#### 2. **Comprehensive Services**
   - **Geek Squad**: BestBuy’s in-house tech support team provides setup, repairs, and troubleshooting for all your devices.
   - **Installation Services**: From home theater systems to appliances, professionals ensure seamless installation.
   - **Protection Plans**: Extended warranties and product replacement services offer peace of mind.

#### 3. **Flexible Shopping Options**
   - **In-Store Pickup**: Reserve products online and pick them up at your nearest store.
   - **Same-Day Delivery**: Get your purchases delivered to your doorstep quickly.
   - **Curbside Pickup**: A convenient and contactless shopping option.

#### 4. **Reward Programs**
BestBuy’s **My Best Buy** program offers exclusive discounts, early access to sales, and points on every purchase that can be redeemed for future discounts.

---

### Online Shopping at BestBuy.com

BestBuy.com provides a seamless shopping experience with features such as:

- **Advanced Search Functionality**: Quickly find products using filters like brand, price range, and specifications.
- **Customer Reviews and Ratings**: Make informed decisions by reading reviews from other customers.
- **Product Recommendations**: AI-powered suggestions based on your browsing and purchase history.
- **Weekly Deals and Promotions**: Access exclusive online-only discounts and limited-time offers.

---

### Environmental Initiatives

BestBuy is committed to sustainability through programs like:
- **Recycling Services**: Drop off old electronics for eco-friendly recycling.
- **Energy-Efficient Products**: A wide selection of ENERGY STAR-certified appliances.
- **Sustainable Packaging**: Efforts to minimize waste and use recyclable materials.

---

### BestBuy in the Community

Beyond retail, BestBuy invests in local communities by:
- Supporting educational programs focused on technology and digital literacy.
- Partnering with non-profits to bridge the digital divide for underserved populations.

---

### Frequently Asked Questions (FAQs)

#### **1. Can I return a product purchased from BestBuy?**
Yes, BestBuy offers a flexible return policy. Most products can be returned within 15 days of purchase. My Best Buy Elite and Elite Plus members enjoy extended return windows.

#### **2. Does BestBuy offer financing options?**
Absolutely! BestBuy provides financing options through the My Best Buy Credit Card, allowing customers to pay for purchases in installments.

#### **3. Can I get my product delivered the same day?**
Yes, same-day delivery is available for select products and locations. Check eligibility during checkout.

#### **4. How can I contact customer service?**
You can reach BestBuy customer service via:
   - **Phone**: Call their helpline for quick assistance.
   - **Online Chat**: Chat with a representative directly on BestBuy.com.
   - **In-Store**: Visit any BestBuy location for support.

#### **5. Is it safe to shop on BestBuy.com?**
Yes, BestBuy.com uses advanced encryption and secure payment gateways to protect your personal and financial information.

#### **6. Does BestBuy price match competitors?**
Yes, BestBuy offers a Price Match Guarantee. If you find a lower price on an identical product at a competitor, BestBuy will match the price.

#### **7. How do I track my online order?**
Log into your BestBuy account, go to the “Order Status” page, and enter your order details to track your shipment.

#### **8. Can I recycle my old electronics at BestBuy?**
Yes, BestBuy has a recycling program where customers can responsibly dispose of old electronics. Some items may even qualify for trade-in credit.

---
