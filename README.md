# msba
  #  class { '::puppet_enterprise':
  #    puppet_master_host              => $primary_master_host,
  #    certificate_authority_host      => $certificate_authority_host,
  #    console_host                    => $console_host,
  #    puppetdb_host                   => $puppetdb_host,
  #    puppetdb_port                   => 5432 , # $puppetdb_port,
  #    database_host                   => $database_host,
  #    mcollective_middleware_hosts    => $_mcollective_middleware_hosts,
  #    dashboard_database_password     => $dashboard_database_password,
  #    puppetdb_database_password      => $puppetdb_database_password,
  #   # activity_database_password      => $activity_database_password,
  #    #classifier_database_password    => $classifier_database_password,
  #    #rbac_database_password          => $rbac_database_password,
  #    #mcollective_middleware_password => $mcollective_middleware_password,
  #    database_ssl                    => false,
  #    pcp_broker_host                 => 'puppet-server-all-in-one.puppet.localdomain', # adding this cos puppet is complaining
  #    console_port                    => 443,
  #  }
  #
  #  class { '::puppet_enterprise::profile::certificate_authority':
  #  }
  #
  #  class { '::puppet_enterprise::profile::mcollective::agent':
  #  }
  #
  #  class { '::puppet_enterprise::profile::master':
  #  }
  #
  #  class { '::puppet_enterprise::profile::mcollective::peadmin':
  #  }
  #
  #  class { '::puppet_enterprise::profile::master::mcollective':
  #  }
  #
  #  class { '::puppet_enterprise::profile::orchestrator':
  #  }
  #
  #  class { '::puppet_enterprise::profile::puppetdb':
  #  }
  #
  #  class { '::puppet_enterprise::profile::console':
  #  }
  #
  #  class { '::pe_console_prune ':
  #  }
  #
  #  class { '::puppet_enterprise::license':
  #  }
  #
  #  class { '::puppet_enterprise::profile::amq::broker':
  #  }
  #
  #  class { '::puppet_enterprise::profile::agent':
  #  }
