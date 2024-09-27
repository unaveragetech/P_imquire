# Upfront Order Form Template

This repository provides a customizable order form template for users who want to build an online submission system to collect customer orders. It’s ideal for businesses selling products like cannabis, concentrates, edibles, or other items.

---

## Table of Contents

1. [Features](#features)
2. [Usage](#usage)
   - [Step 1: Clone the Repository](#step-1-clone-the-repository)
   - [Step 2: Modify the Template](#step-2-modify-the-template)
   - [Step 3: Test the Form](#step-3-test-the-form)
   - [Step 4: Deploy](#step-4-deploy)
   - [Step 5: View Submissions](#step-5-view-submissions)
3. [FormSubmit Decorators](#formsubmit-decorators)
4. [Customization Instructions](#customization-instructions)
5. [License](#license)

---

## Features

- **Customizable Form Fields**: Easily modify product selections, customer input fields, and order submission fields.
- **Simple Design**: Clean, modern design with form validation to ensure accurate order submissions.
- **Order Submissions via GitHub**: View customer order submissions directly from your GitHub repository using a backend form handling solution like FormSubmit.
- **Third-Party Integration**: Easily integrate with third-party delivery services or payment processing platforms.

- cant code no problem
https://websim.ai/@brightrain79844418/upfront-order-form-tutorial
---

## Usage

### Step 1: Clone the Repository

Clone this repository to your local machine to begin working with the template.

```bash
git clone https://github.com/unaveragetech/P_imquire.git
cd P_imquire
```

### Step 2: Modify the Template

You’ll need to customize the form to fit your business’s needs. This includes:

1. **Update Product Options**: Modify the product selection dropdown to match the items you offer.
2. **Add Custom Branding**: Replace the header and footer content with your business’s branding, logos, and contact information.
3. **Edit Submission Handling**: Update the form's action URL to point to your desired form handling solution, such as FormSubmit or a custom backend.

### Step 3: Test the Form

Ensure all form fields work as expected and data is properly collected. You can test form submissions locally or deploy the site to a hosting platform like GitHub Pages to test in production.

### Step 4: Deploy

When you're satisfied with the form, deploy it to a web hosting provider. For GitHub users, GitHub Pages is a great option to host the form for free.

1. Enable GitHub Pages for the repository.
2. Push your changes to the `main` branch, and GitHub Pages will host your site.

```bash
git add .
git commit -m "Customized the form"
git push origin main
```

### Step 5: View Submissions

If using a service like FormSubmit, you can set up submissions to be sent to your email or store them in your GitHub repository for viewing.

---

## FormSubmit Decorators

FormSubmit offers a variety of decorators you can use to customize the behavior of your form. Here's a breakdown of the most commonly used decorators and how to implement them:

| **Decorator**   | **Usage**                                      | **Example**                                                                 |
|-----------------|------------------------------------------------|-----------------------------------------------------------------------------|
| `_replyto`      | Sets the email's Reply-To field for easy replies to the user. | `<input type="email" name="email" placeholder="Email Address">`              |
| `_next`         | Redirects users to a custom URL after form submission. | `<input type="hidden" name="_next" value="https://yourdomain.co/thanks.html">` |
| `_subject`      | Specifies the subject line for the email.       | `<input type="hidden" name="_subject" value="New submission!">`             |
| `_cc`           | Sends a copy of the submission to another email. Supports multiple email addresses separated by commas. | `<input type="hidden" name="_cc" value="another@email.com,yetanother@email.com">` |
| `_blacklist`    | Filters out submissions containing certain phrases to reduce spam. | `<input type="hidden" name="_blacklist" value="spammy pattern, banned term">` |
| `_captcha`      | Disables reCAPTCHA for the form (not recommended to avoid spam). | `<input type="hidden" name="_captcha" value="false">`                       |
| `_honey`        | Adds a honeypot field to catch bots and prevent spam submissions. Should be hidden via CSS. | `<input type="text" name="_honey" style="display:none">`                    |
| `_autoresponse` | Sends an automatic response to the user after form submission. Requires an email input field. | `<input type="hidden" name="_autoresponse" value="Thank you for your submission!">` |
| `_template`     | Specifies which email template to use (e.g., table, basic). | `<input type="hidden" name="_template" value="table">`                      |
| `_webhook`      | Sends form data to a specified webhook URL for real-time data manipulation. | `<input type="hidden" name="_webhook" value="https://yourdomain.co/webhook">` |
| **Invisible Email** | Hides your email from bots by using a random-like string instead of your email address. | `<form action="https://formsubmit.co/random-string" method="POST">`         |
| **File Uploads** | Allows file uploads (up to 5MB total), requires `enctype="multipart/form-data"`. | `<input type="file" name="attachment" accept="image/png, image/jpeg">`      |
| **AJAX Forms**  | Submits the form via AJAX without page reload.  | `$.ajax({ url: "https://formsubmit.co/ajax/your@email.com", method: "POST", data: { name: "FormSubmit", message: "Hello!" }, dataType: "json" });` |
| **Unlimited Forms** | Allows unlimited forms and submissions for a single email address. | Not applicable                                                              |
| **Submissions Archive** | Access previous form submissions via the FormSubmit API. | Not applicable                                                              |

---

## Customization Instructions

This template should be **extensively modified** before deployment. Some key areas to customize include:

- **Business Information**: Update the company name, product descriptions, and legal information to match your business.
- **Styling**: Modify the CSS and overall style to fit your branding.
- **Form Fields**: Add or remove form fields as needed, depending on your product and service offerings.

### Example Modifications

1. **Customizing Product Options**: To change the product options, locate the product selection field in the `index.html` file and edit the values.

```html
<select class="form-select" name="productSelection">
    <option value="flower">Cannabis Flower</option>
    <option value="oil">Concentrates (Oils)</option>
    <option value="edibles">Edibles</option>
    <option value="custom">Custom Order</option>
</select>
```

2. **FormSubmit Integration**: Update the form action to submit to FormSubmit or your own backend solution.

```html
<form action="https://formsubmit.co/your-email@example.com" method="POST">
```

---

## License

SDUC
