---
title: Upgrading RubyGems 0.9.5 to 1.0.1
author: Danesh
date: 2007-12-22T12:20:16+00:00
pvc_views:
  - 7279
dsq_thread_id:
  - 889737987

---
![][1]

Upgraded my [Rails to 2.0.2][2] and [RubyGems to 1.0.1][3].

  1. _**gem &#8211;version**_ to check your gems version.
  2. _**sudo gem update**_ &#8211;system to update your gems.
  3. _**sudo gem install rails**_ to update rails to the latest version.

See outputs on the next page&#8230;..  
<!--more-->

  
`danny@pandora:~> gem --version<br />
0.9.5<br />
danny@pandora:~> sudo gem update --system<br />
Updating RubyGems...<br />
Updating metadata for 130 gems from http://gems.rubyforge.org<br />
.........................................................................................<br />
.........................................<br />
complete<br />
Attempting remote update of rubygems-update<br />
Successfully installed rubygems-update-1.0.1<br />
1 gem installed<br />
Updating version of RubyGems to 1.0.1<br />
Installing RubyGems 1.0.1<br />
install -c -m 0644 rubygems/dependency.rb /usr/lib/ruby/site_ruby/1.8/rubygems/dependency<br />
.rb<br />
install -c -m 0644 rubygems/source_index.rb /usr/lib/ruby/site_ruby/1.8/rubygems/source_i<br />
ndex.rb<br />
install -c -m 0644 rubygems/config_file.rb /usr/lib/ruby/site_ruby/1.8/rubygems/config_fi<br />
le.rb<br />
install -c -m 0644 rubygems/requirement.rb /usr/lib/ruby/site_ruby/1.8/rubygems/requireme<br />
nt.rb<br />
install -c -m 0644 rubygems/doc_manager.rb /usr/lib/ruby/site_ruby/1.8/rubygems/doc_manag<br />
er.rb<br />
install -c -m 0644 rubygems/ext/builder.rb /usr/lib/ruby/site_ruby/1.8/rubygems/ext/build<br />
er.rb<br />
install -c -m 0644 rubygems/ext/configure_builder.rb /usr/lib/ruby/site_ruby/1.8/rubygems<br />
/ext/configure_builder.rb<br />
install -c -m 0644 rubygems/ext/ext_conf_builder.rb /usr/lib/ruby/site_ruby/1.8/rubygems/<br />
ext/ext_conf_builder.rb<br />
install -c -m 0644 rubygems/ext/rake_builder.rb /usr/lib/ruby/site_ruby/1.8/rubygems/ext/<br />
rake_builder.rb<br />
install -c -m 0644 rubygems/source_info_cache_entry.rb /usr/lib/ruby/site_ruby/1.8/rubyge<br />
ms/source_info_cache_entry.rb<br />
install -c -m 0644 rubygems/gem_runner.rb /usr/lib/ruby/site_ruby/1.8/rubygems/gem_runner<br />
.rb<br />
install -c -m 0644 rubygems/builder.rb /usr/lib/ruby/site_ruby/1.8/rubygems/builder.rb<br />
install -c -m 0644 rubygems/validator.rb /usr/lib/ruby/site_ruby/1.8/rubygems/validator.r<br />
b<br />
install -c -m 0644 rubygems/digest/digest_adapter.rb /usr/lib/ruby/site_ruby/1.8/rubygems<br />
/digest/digest_adapter.rb<br />
install -c -m 0644 rubygems/digest/sha1.rb /usr/lib/ruby/site_ruby/1.8/rubygems/digest/sh<br />
a1.rb<br />
install -c -m 0644 rubygems/digest/sha2.rb /usr/lib/ruby/site_ruby/1.8/rubygems/digest/sh<br />
a2.rb<br />
install -c -m 0644 rubygems/digest/md5.rb /usr/lib/ruby/site_ruby/1.8/rubygems/digest/md5<br />
.rb<br />
install -c -m 0644 rubygems/custom_require.rb /usr/lib/ruby/site_ruby/1.8/rubygems/custom<br />
_require.rb<br />
install -c -m 0644 rubygems/security.rb /usr/lib/ruby/site_ruby/1.8/rubygems/security.rb<br />
install -c -m 0644 rubygems/version.rb /usr/lib/ruby/site_ruby/1.8/rubygems/version.rb<br />
install -c -m 0644 rubygems/rubygems_version.rb /usr/lib/ruby/site_ruby/1.8/rubygems/ruby<br />
gems_version.rb<br />
install -c -m 0644 rubygems/server.rb /usr/lib/ruby/site_ruby/1.8/rubygems/server.rb<br />
install -c -m 0644 rubygems/defaults.rb /usr/lib/ruby/site_ruby/1.8/rubygems/defaults.rb<br />
install -c -m 0644 rubygems/timer.rb /usr/lib/ruby/site_ruby/1.8/rubygems/timer.rb<br />
install -c -m 0644 rubygems/source_info_cache.rb /usr/lib/ruby/site_ruby/1.8/rubygems/sou<br />
rce_info_cache.rb<br />
install -c -m 0644 rubygems/require_paths_builder.rb /usr/lib/ruby/site_ruby/1.8/rubygems<br />
/require_paths_builder.rb<br />
install -c -m 0644 rubygems/dependency_list.rb /usr/lib/ruby/site_ruby/1.8/rubygems/depen<br />
dency_list.rb<br />
install -c -m 0644 rubygems/indexer/master_index_builder.rb /usr/lib/ruby/site_ruby/1.8/r<br />
ubygems/indexer/master_index_builder.rb<br />
install -c -m 0644 rubygems/indexer/marshal_index_builder.rb /usr/lib/ruby/site_ruby/1.8/<br />
rubygems/indexer/marshal_index_builder.rb<br />
install -c -m 0644 rubygems/indexer/abstract_index_builder.rb /usr/lib/ruby/site_ruby/1.8<br />
/rubygems/indexer/abstract_index_builder.rb<br />
install -c -m 0644 rubygems/indexer/quick_index_builder.rb /usr/lib/ruby/site_ruby/1.8/ru<br />
bygems/indexer/quick_index_builder.rb<br />
install -c -m 0644 rubygems/specification.rb /usr/lib/ruby/site_ruby/1.8/rubygems/specifi<br />
cation.rb<br />
install -c -m 0644 rubygems/uninstaller.rb /usr/lib/ruby/site_ruby/1.8/rubygems/uninstall<br />
er.rb<br />
install -c -m 0644 rubygems/platform.rb /usr/lib/ruby/site_ruby/1.8/rubygems/platform.rb<br />
install -c -m 0644 rubygems/format.rb /usr/lib/ruby/site_ruby/1.8/rubygems/format.rb<br />
install -c -m 0644 rubygems/gem_path_searcher.rb /usr/lib/ruby/site_ruby/1.8/rubygems/gem<br />
_path_searcher.rb<br />
install -c -m 0644 rubygems/old_format.rb /usr/lib/ruby/site_ruby/1.8/rubygems/old_format<br />
.rb<br />
install -c -m 0644 rubygems/command.rb /usr/lib/ruby/site_ruby/1.8/rubygems/command.rb<br />
install -c -m 0644 rubygems/remote_fetcher.rb /usr/lib/ruby/site_ruby/1.8/rubygems/remote<br />
_fetcher.rb<br />
install -c -m 0644 rubygems/package.rb /usr/lib/ruby/site_ruby/1.8/rubygems/package.rb<br />
install -c -m 0644 rubygems/dependency_installer.rb /usr/lib/ruby/site_ruby/1.8/rubygems/<br />
dependency_installer.rb<br />
install -c -m 0644 rubygems/command_manager.rb /usr/lib/ruby/site_ruby/1.8/rubygems/comma<br />
nd_manager.rb<br />
install -c -m 0644 rubygems/indexer.rb /usr/lib/ruby/site_ruby/1.8/rubygems/indexer.rb<br />
install -c -m 0644 rubygems/ext.rb /usr/lib/ruby/site_ruby/1.8/rubygems/ext.rb<br />
install -c -m 0644 rubygems/gem_open_uri.rb /usr/lib/ruby/site_ruby/1.8/rubygems/gem_open<br />
_uri.rb<br />
install -c -m 0644 rubygems/install_update_options.rb /usr/lib/ruby/site_ruby/1.8/rubygem<br />
s/install_update_options.rb<br />
install -c -m 0644 rubygems/gem_openssl.rb /usr/lib/ruby/site_ruby/1.8/rubygems/gem_opens<br />
sl.rb<br />
install -c -m 0644 rubygems/version_option.rb /usr/lib/ruby/site_ruby/1.8/rubygems/versio<br />
n_option.rb<br />
install -c -m 0644 rubygems/local_remote_options.rb /usr/lib/ruby/site_ruby/1.8/rubygems/<br />
local_remote_options.rb<br />
install -c -m 0644 rubygems/commands/generate_index_command.rb /usr/lib/ruby/site_ruby/1.<br />
8/rubygems/commands/generate_index_command.rb<br />
install -c -m 0644 rubygems/commands/outdated_command.rb /usr/lib/ruby/site_ruby/1.8/ruby<br />
gems/commands/outdated_command.rb<br />
install -c -m 0644 rubygems/commands/sources_command.rb /usr/lib/ruby/site_ruby/1.8/rubyg<br />
ems/commands/sources_command.rb<br />
install -c -m 0644 rubygems/commands/check_command.rb /usr/lib/ruby/site_ruby/1.8/rubygem<br />
s/commands/check_command.rb<br />
install -c -m 0644 rubygems/commands/cleanup_command.rb /usr/lib/ruby/site_ruby/1.8/rubyg<br />
ems/commands/cleanup_command.rb<br />
install -c -m 0644 rubygems/commands/specification_command.rb /usr/lib/ruby/site_ruby/1.8<br />
/rubygems/commands/specification_command.rb<br />
install -c -m 0644 rubygems/commands/unpack_command.rb /usr/lib/ruby/site_ruby/1.8/rubyge<br />
ms/commands/unpack_command.rb<br />
install -c -m 0644 rubygems/commands/build_command.rb /usr/lib/ruby/site_ruby/1.8/rubygem<br />
s/commands/build_command.rb<br />
install -c -m 0644 rubygems/commands/rdoc_command.rb /usr/lib/ruby/site_ruby/1.8/rubygems<br />
/commands/rdoc_command.rb<br />
install -c -m 0644 rubygems/commands/lock_command.rb /usr/lib/ruby/site_ruby/1.8/rubygems<br />
/commands/lock_command.rb<br />
install -c -m 0644 rubygems/commands/environment_command.rb /usr/lib/ruby/site_ruby/1.8/r<br />
ubygems/commands/environment_command.rb<br />
install -c -m 0644 rubygems/commands/search_command.rb /usr/lib/ruby/site_ruby/1.8/rubyge<br />
ms/commands/search_command.rb<br />
install -c -m 0644 rubygems/commands/fetch_command.rb /usr/lib/ruby/site_ruby/1.8/rubygem<br />
s/commands/fetch_command.rb<br />
install -c -m 0644 rubygems/commands/dependency_command.rb /usr/lib/ruby/site_ruby/1.8/ru<br />
bygems/commands/dependency_command.rb<br />
install -c -m 0644 rubygems/commands/cert_command.rb /usr/lib/ruby/site_ruby/1.8/rubygems<br />
/commands/cert_command.rb<br />
install -c -m 0644 rubygems/commands/help_command.rb /usr/lib/ruby/site_ruby/1.8/rubygems<br />
/commands/help_command.rb<br />
install -c -m 0644 rubygems/commands/uninstall_command.rb /usr/lib/ruby/site_ruby/1.8/rub<br />
ygems/commands/uninstall_command.rb<br />
install -c -m 0644 rubygems/commands/contents_command.rb /usr/lib/ruby/site_ruby/1.8/ruby<br />
gems/commands/contents_command.rb<br />
install -c -m 0644 rubygems/commands/list_command.rb /usr/lib/ruby/site_ruby/1.8/rubygems<br />
/commands/list_command.rb<br />
install -c -m 0644 rubygems/commands/install_command.rb /usr/lib/ruby/site_ruby/1.8/rubyg<br />
ems/commands/install_command.rb<br />
install -c -m 0644 rubygems/commands/query_command.rb /usr/lib/ruby/site_ruby/1.8/rubygem                                                  s/commands/query_command.rb<br />
install -c -m 0644 rubygems/commands/update_command.rb /usr/lib/ruby/site_ruby/1.8/rubyge                                                  ms/commands/update_command.rb<br />
install -c -m 0644 rubygems/commands/pristine_command.rb /usr/lib/ruby/site_ruby/1.8/ruby                                                  gems/commands/pristine_command.rb<br />
install -c -m 0644 rubygems/commands/mirror_command.rb /usr/lib/ruby/site_ruby/1.8/rubyge                                                  ms/commands/mirror_command.rb<br />
install -c -m 0644 rubygems/commands/which_command.rb /usr/lib/ruby/site_ruby/1.8/rubygem                                                  s/commands/which_command.rb<br />
install -c -m 0644 rubygems/commands/server_command.rb /usr/lib/ruby/site_ruby/1.8/rubyge                                                  ms/commands/server_command.rb<br />
install -c -m 0644 rubygems/installer.rb /usr/lib/ruby/site_ruby/1.8/rubygems/installer.r                                                  b<br />
install -c -m 0644 rubygems/user_interaction.rb /usr/lib/ruby/site_ruby/1.8/rubygems/user                                                  _interaction.rb<br />
install -c -m 0644 rubygems/exceptions.rb /usr/lib/ruby/site_ruby/1.8/rubygems/exceptions                                                  .rb<br />
install -c -m 0644 rubygems/open-uri.rb /usr/lib/ruby/site_ruby/1.8/rubygems/open-uri.rb<br />
install -c -m 0644 rbconfig/datadir.rb /usr/lib/ruby/site_ruby/1.8/rbconfig/datadir.rb<br />
install -c -m 0644 ubygems.rb /usr/lib/ruby/site_ruby/1.8/ubygems.rb<br />
install -c -m 0644 rubygems.rb /usr/lib/ruby/site_ruby/1.8/rubygems.rb<br />
cp gem /tmp/gem<br />
install -c -m 0755 /tmp/gem /usr/bin/gem<br />
rm /tmp/gem<br />
cp update_rubygems /tmp/update_rubygems<br />
install -c -m 0755 /tmp/update_rubygems /usr/bin/update_rubygems<br />
rm /tmp/update_rubygems<br />
rm /usr/lib/ruby/gems/1.8/source_cache<br />
Removing old RubyGems RDoc and ri...<br />
rm -rf /usr/lib/ruby/gems/1.8/doc/rubygems-0.9.5<br />
Installing rubygems-1.0.1 ri into /usr/lib/ruby/gems/1.8/doc/rubygems-1.0.1/ri...<br />
Installing rubygems-1.0.1 rdoc into /usr/lib/ruby/gems/1.8/doc/rubygems-1.0.1/rdoc...<br />
As of RubyGems 0.8.0, library stubs are no longer needed.<br />
Searching $LOAD_PATH for stubs to optionally delete (may take a while)...<br />
...done.<br />
No library stubs found.<br />
RubyGems system software updated<br />
danny@pandora:~> gem<br />
gem       gemtopbm  gemtopnm<br />
danny@pandora:~> sudo gem install rails<br />
Bulk updating Gem source index for: http://gems.rubyforge.org<br />
Successfully installed rake-0.8.0<br />
Successfully installed activesupport-2.0.2<br />
Successfully installed activerecord-2.0.2<br />
Successfully installed actionpack-2.0.2<br />
Successfully installed actionmailer-2.0.2<br />
Successfully installed activeresource-2.0.2<br />
Successfully installed rails-2.0.2<br />
7 gems installed<br />
Installing ri documentation for rake-0.8.0...<br />
Installing ri documentation for activesupport-2.0.2...<br />
Installing ri documentation for activerecord-2.0.2...<br />
Installing ri documentation for actionpack-2.0.2...<br />
Installing ri documentation for actionmailer-2.0.2...<br />
Installing ri documentation for activeresource-2.0.2...<br />
Installing RDoc documentation for rake-0.8.0...<br />
Installing RDoc documentation for activesupport-2.0.2...<br />
Installing RDoc documentation for activerecord-2.0.2...<br />
Installing RDoc documentation for actionpack-2.0.2...<br />
Installing RDoc documentation for actionmailer-2.0.2...<br />
Installing RDoc documentation for activeresource-2.0.2...<br />
danny@pandora:~>`

 [1]: http://img179.imageshack.us/img179/2953/railsdh7.png
 [2]: http://weblog.rubyonrails.org/2007/12/17/rails-2-0-2-some-new-defaults-and-a-few-fixes
 [3]: http://weblog.rubyonrails.org/2007/12/19/trouble-installing-new-gems