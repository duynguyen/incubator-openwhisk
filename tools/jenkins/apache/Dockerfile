FROM couchdb:1.6

RUN apt-get update && apt-get install jq

COPY import /import
COPY import.sh /import.sh
COPY init.sh /init.sh

RUN chmod +x /import.sh
RUN chmod +x /init.sh

ENTRYPOINT ["tini", "--", "/init.sh"]
CMD ["couchdb"]
