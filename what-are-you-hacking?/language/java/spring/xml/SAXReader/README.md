# SAXReader
## Insecure
```
public class SAXReaderXMLInjectionExample() {
    public void main(String[] args) {
        try {
            SAXReader reader = new SAXReader();
            Document document = reader.read( file.getInputStream() );
            List<Node> nodes = document.selectNodes("//employees/employee");
        }
    }
}
```
## Secure
```
public class SAXReaderXMLInjectionExample() {
    public void main(String[] args) {
        try {
            SAXReader reader = new SAXReader();
            reader.setFeature( DISALLOW_DOCTYPE_DECL_FEATURE, true);
            Document document = reader.read( file.getInputStream() );
            List<Node> nodes = document.selectNodes("//employees/employee");
        }
    }
}
```
## Explanation
The safest way to prevent XXE is always to disable DTDs (External Entities) completely. Depending on the parser, the method should be similar to the following:

`factory.setFeature("http://apache.org/xml/features/disallow-doctype-decl", true);`

Disabling DTDs also makes the parser secure against denial of services (DOS) attacks such as Billion Laughs. If it is not possible to disable DTDs completely, then external entities and external document type declarations must be disabled in the way that's specific to each parser.

If you are unable to disable using the above, then you must use the following two together to disable DTDs and prevent XML
`factory.setFeature("http://xml.org/sax/features/external-general-entities", false);`
`factory.setFeature("http://xml.org/sax/features/external-parameter-entities", false);`

## Exploit Example
<!DOCTYPE foo [<!ENTITY xxe SYSTEM "/etc/shadow"> ]>

## links
OWASP XXE Prevention link: https://cheatsheetseries.owasp.org/cheatsheets/XML_External_Entity_Prevention_Cheat_Sheet.html