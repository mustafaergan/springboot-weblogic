SpringBootServletInitializer extend edilip WebApplicationInitializer implements edildikten sonra configure ovirride edilir.

Spring boot classımız sources olarak belirtilir.

```
    extends SpringBootServletInitializer implements WebApplicationInitializer

    @Override
    protected SpringApplicationBuilder configure(SpringApplicationBuilder builder) {
        return builder.sources(WeblogicApplication.class);
    }
```

Main altında webapp diye bir klasör oluşturulur ve web-inf klasörü altında weblogic.xml oluşturulur. Proje tarafından yönetilen paket isimleri belirtilir.  dispatcherServlet-servlet.xml oluşturulur.

```
        <wls:prefer-application-packages>
            <wls:package-name>org.springframework.*</wls:package-name>
            <wls:package-name>org.hibernate.*</wls:package-name>
            <wls:package-name>javax.validation.*</wls:package-name>
            <wls:package-name>org.jboss.*</wls:package-name>
            <wls:package-name>org.joda.*</wls:package-name>
            <wls:package-name>org.slf4j.*</wls:package-name>
            <wls:package-name>com.fasterxml.*</wls:package-name>
        </wls:prefer-application-packages>
```


