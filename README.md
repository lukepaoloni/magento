# Magento 2 Boilderplate
### This is a curated list of all the Magento 2 extensions I use.

## Development:
<ol>
    <li>
        <dl>
            <dt>
                <a href="https://github.com/ho-nl/magento2-Ho_Templatehints">Template Hints</a>
                <br/><br/>
                <img src="https://github.com/ho-nl/magento2-Ho_Templatehints/raw/master/docs/usage.gif" />
            </dt>
            <dd><code>composer require honl/magento2-templatehints</code></dd>
            <dd><code>php bin/magento module:enable Ho_Templatehints</code></dd>
            <dd><code>php bin/magento setup:upgrade</code></dd>
        </dl>
    </li>
    <li>
        <dl>
            <dt>
                <a href="https://github.com/mgtcommerce/Mgt_Developertoolbar">Developer Toolbar</a>
                <br/><br/>
                <img src="https://github.com/mgtcommerce/Mgt_Developertoolbar/raw/master/doc/static_files/profiler.png" />
            </dt>
            <dd><code>composer require mgtcommerce/module-mgtdevelopertoolbar</code></dd>
            <dd><code>php bin/magento setup:upgrade</code></dd>
            <dd><code>rm -rf pub/static/* </code></dd>
            <dd><code>rm -rf var/*</code></dd>
            <dd><code>php bin/magento setup:static-content:deploy </code></dd>
        </dl>
    </li>
    <li>
        <dl>
            <dt>
                <a href="https://github.com/magento-ecg/coding-standard">PHP Magento CodeSniffer Coding Standard</a>
            </dt>
            <dd><code>composer global require "squizlabs/php_codesniffer=*"</code></dd>
            <dd><code>composer require magento-ecg/coding-standard</code></dd>
        </dl>
        Usage

Select a standard to run with CodeSniffer:

* Ecg for Magento
* EcgM2 for Magento 2

Run CodeSniffer:

```sh
$ phpcs --standard=./vendor/magento-ecg/coding-standard/Ecg /path/to/code
```
```sh
$ phpcs --standard=./vendor/magento-ecg/coding-standard/EcgM2 /path/to/code
```

As a one time thing, you can add the ECG standards directory to PHP_CodeSniffer's installed paths:
```sh
$ phpcs --config-set installed_paths /path/to/your/folder/vendor/magento-ecg/coding-standard
```

After that specifying the path to a standard is optional:
```sh
$ phpcs --standard=Ecg /path/to/code
```
```sh
$ phpcs --standard=EcgM2 /path/to/code
```

PHP CodeSniffer will automatically scan Magento PHP files. To check design templates, you must specify `phtml` in the `--extensions` argument: `--extensions=php,phtml`.
    </li>
    <li>
        <dl>
            <dt>
                <a href="https://github.com/yireo/Yireo_Whoops">Whoops! Exception Notice</a>
                <br/><br/>
                <img src="https://daveismyname.blog/assets/images/blog/laravel-framework/whoops.png" />
            </dt>
            <dd><code>composer require --dev yireo/magento2-whoops</code></dd>
            <dd><code>php bin/magento setup:upgrade</code></dd>
        </dl>
    </li>
    <li>
        <dl>
            <dt>
                <a href="https://github.com/SnowdogApps/magento2-frontools">Front-End Tools using Gulp.js</a>
                <br/><br/>
            </dt>
            <dd>Run <code>composer require snowdog/frontools</code></dd>
            <dd>Go to package directory <code>cd vendor/snowdog/frontools</code></dd>
            <dd>Run <code>npm install</code></dd>
        </dl>
    </li>
    <li>
        <dl>
            <dt>
                <a href="https://github.com/SnowdogApps/magento2-theme-blank-sass">SASS Based version of Magento 2 Blank Theme</a>
                <br/><br/>
            </dt>
            <dd>Run in root magento folder <code>composer require snowdog/theme-blank-sass</code></dd>
            <dd>Set you application to <code>developer</code> mode</dd>
            <dd>Run <code>bin/magento setup:upgrade</code> to register theme</dd>
            <dd>Compile SASS using frontools </dd>
        </dl>
    </li>
    <li>
        <dl>
            <h4> Optional:</h4>
            <dt>
                <a href="https://github.com/SnowdogApps/magento2-menu">Menu Management</a>
                <br/><br/>
            </dt>
            <dd>Go to Magento module root folder <code>cd app/code</code></dd>
            <dd>Create folder <code>mkdir Snowdog</code></dd>
            <dd>Go inside that folder <code>cd Snowdog</code></dd>
            <dd>Clone <code>git clone https://github.com/SnowdogApps/magento2-menu.git Menu </code></dd>
            <dd>Setup upgrade <code>php bin/magento setup:upgrade </code></dd>
        </dl>
    </li>
</ol>

## Production:
- [Two Factor Authentication](https://github.com/magespecialist/m2-MSP_TwoFactorAuth) - `composer require msp/twofactorauth`
- [SEO Extension](https://github.com/mageplaza/magento-2-seo) - `composer require mageplaza/magento-2-seo-extension`
- [MailChimp Integration](https://marketplace.magento.com/mailchimp-mc-magento2.html)
- [Blog](https://github.com/mageplaza/magento-2-blog) - 
`cd app/codemkdir Mageplaza git clone https://github.com/mageplaza/magento-2-blog.git Blog`
