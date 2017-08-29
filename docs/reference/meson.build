docs_conf = configuration_data ()
docs_conf.set ('LIBCLOUDPROVIDERS_VERSION_INFO', meson.project_version())

docs_version = configure_file (input: 'version.xml.in',
                               output: 'version.xml',
                               configuration: docs_conf)

gnome.gtkdoc ('libcloudproviders',
              main_xml: 'libcloudproviders-docs.xml',
              src_dir: meson.source_root(),
              install: true) 
