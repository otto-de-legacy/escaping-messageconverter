#escaping-messageconverter

Simple message converter for logback that escapes quotation marks to make json-logging easier.
```clojure
[de.otto/escaping-messageconverter "0.1.1"]
```


## Usage

You can reference it in your ```logback.xml``` like this:

```xml
<conversionRule conversionWord="mescaped"
                       converterClass="de.otto.util.escapingmessageconverter" />
```

and then use it in a pattern like this:

```xml
<encoder>
    <pattern>%d{ISO8601} %-5p logger=%c thread=%t  msg="%mescaped"%n</pattern>
</encoder>
```

## Price

If you know a way to do that with logback alone, you win a price of little or no monetary value.


## License
Apache License
