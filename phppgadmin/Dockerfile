# Inspired by https://github.com/maxexcloo/Docker/blob/master/applications/phppgadmin/Dockerfile

FROM maxexcloo/phppgadmin
RUN echo "\$conf['extra_login_security'] = false;" >> /data/http/conf/config.inc.php
RUN wget http://oscg-downloads.s3.amazonaws.com/packages/postgresql-9.5.0-1-x64-bigsql.deb
RUN dpkg -i postgresql-9.5.0-1-x64-bigsql.deb 
RUN echo "\$conf['servers'][0]['pg_dump_path'] = '/opt/postgresql/pg95/bin/pg_dump';\n" >> /data/http/conf/config.inc.php
RUN echo "\$conf['servers'][0]['pg_dumpall_path'] = '/opt/postgresql/pg95/bin/pg_dumpall';\n" >> /data/http/conf/config.inc.php

