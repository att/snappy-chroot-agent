# Snappy-Chroot-Agent
A chroot container for a Snappy Agent

Current functions:  
- translate a Cinder ID to its backing type and ID
- translate a Cinder Name to its Cinder ID

These functions are used by the Snappy Frontend.

The agent maybe be placed in the same location as the Snappy Frontend. If access to the Cinder (Openstack) database is limited by a firewall, it can be placed behind the firewall with an port open so the Frontend can connect to it.  The Frontend should be in an easily accessible location so that it can receive requests.


Unpack the tar.gz file:  
  cd /  
  tar xzvf snappy-agent-chroot-vx.y.z.tgz   

Before starting two things need to be done:  

1) Fill out the environment variables:  
  /srv/snappy-agent/bin/edit_env_vars  
  
2) Verify that the database connection(s) are working, as specified above:  
  /srv/snappy-mysql/bin/edit_tables  


To start the Agent: /srv/snappy-agent/bin/start [port_number]  
To stop the Agent:  /srv/snappy-agent/bin/stop  

By default the Frontend will run on port 8080
