# AEM Hello World Preview-Publish-Dispatcher

[![Build Status][badge]][ci]

This is an example AEM Hello World artifact that will be deployed to an AEM
Preview-Publish-Dispatcher instance.

This artifact contains:

* [Apache configuration template(s)][apache-conf] in `apache-conf-templates`
  directory
* [Apache Virtual Host template(s)][apache-vhosts] and
  [Apache RewriteMap template(s)][apache-rewritemap] in
  `virtual-hosts-templates` directory
* [AEM Dispatcher configuration template(s)][dispatcher-conf] in
  `dispatcher-conf-templates` directory
* Static files in `static-assets` directory

Template files are written in [Embedded Puppet template syntax][epp].

Check out [Dispatcher Template Parameters][template-params] for a list of
available parameters to be used from EPP template files.

## Usage

To create artifact zip file:

```shell
make package
```

The artifact will be written at
`stage/aem-helloworld-preview-publish-dispatcher-<version>.zip`

### Troubleshooting

After the deployment of AEM Hello World Preview-Publish-Dispatcher artifact
and [AEM Hello World][aem-helloworld] package, the following URL paths should
be accessible via AEM Preview-Publish-Dispatcher instance:

* `/content/helloworld` - Hello World page served from AEM Publish instance
* `/cafe-helloworld` - a rewrite rule (using relative path) configured in
  Preview-Publish-Dispatcher instance
* `/cafe/helloworld` - a rewrite rule (using absolute path) configured in
  Preview-Publish-Dispatcher instance
* `/images/earth.jpg` - a sample static asset image served from Apache docroot

[badge]: https://github.com/shinesolutions/aem-helloworld-preview-publish-dispatcher/workflows/CI/badge.svg
[ci]: https://github.com/shinesolutions/aem-helloworld-publish-dispatcher/actions?query=workflow%3ACI
[apache-conf]: https://httpd.apache.org/docs/2.4/configuring.html
[apache-vhosts]: https://httpd.apache.org/docs/2.4/vhosts/
[apache-rewritemap]: https://httpd.apache.org/docs/current/rewrite/rewritemap.html
[dispatcher-conf]: https://docs.adobe.com/docs/en/dispatcher/disp-config.html
[epp]: https://docs.puppet.com/puppet/4.10/lang_template_epp.html
[template-params]: https://github.com/shinesolutions/puppet-aem-curator/blob/main/docs/dispatcher-template-parameters.md
[aem-helloworld]: https://github.com/shinesolutions/aem-helloworld/
