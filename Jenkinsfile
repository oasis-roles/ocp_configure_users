library('oasis-pipeline')

oasisMultistreamMoleculePipeline {
  upstream_git_url = 'https://github.com/oasis-roles/ocp_configure_users.git'
  molecule_role_name = 'ocp_configure_users'
  molecule_scenarios = ['openstack']
  properties = [pipelineTriggers([cron('H H * * *')])]
}