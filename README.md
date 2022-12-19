# Data Repository for reports.report

This is the data that [reports.report](https://reports.report) uses to display the site.

## Contributing

If you wish to add your site to the list, then read on!

### 1. Prerequisites

* Your site must be accessible via a domain with a `.report` TLD.
* Your site must be functional and somewhat polished.
* Your site must offer a service, info, data, or similar; relating to Destiny.
* Your site must be original work.

### 2. Data Format

The data is in XML format. Every site is a `<report>` element. Every `<report>` element contains:

* `<host>`: This is your host part - if your website was `foobar.reports`, then the element would
  be `<host>foobar</host>`.
* `<description>`: A short description of your page.
    * Must be less than 300 characters.
    * This is not an advertising space, therefore, keep it cool with the superlatives. Instead of "The ultimate guide to
      Crucible stats with the best visuals", try "A visual guide to Crucible stats".
* optional: `<stylized_name>`: In case your capitalization (!) is different from Start Case, you can use a stylized
  name.
    * For example, `twab.report` should not be displayed as `Twab.Report`, so we
      use `<stylized_name>TWAB</stylized_name>` to have it display as `TWAB.Report`.
    * *Your `<host>` and your `<stylized_name>` must match exactly when converted to lowercase.*

### 3. Pull Request

In your pull request, add a `<report>` element below the last existing element.

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<reports>
    <!--  ...other elements here...  -->
+   <report>
+       <host>foobar</host>
+       <stylized_name>FooBar</stylized_name> <!-- stylized_name is optional -->
+       <description>
+           A site to display sample values of FooBar in Destiny.
+       </description>
+   </report>
</reports>
```

Your request will get validated against the schema. Validation has to pass for your request to be considered.

---

reports.report by [nwL](https://nwl.gg)
