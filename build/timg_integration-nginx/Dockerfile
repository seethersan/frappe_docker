FROM bitnami/node:12-prod

COPY install_app.sh /install_app

RUN /install_app timg_integration https://github.com/seethersan/timg_integration version-12

FROM frappe/erpnext-nginx:edge

COPY --from=0 /home/frappe/frappe-bench/sites/ /var/www/html/
COPY --from=0 /rsync /rsync
RUN echo -n "\ntimg_integration" >> /var/www/html/apps.txt

VOLUME [ "/assets" ]

ENTRYPOINT ["/docker-entrypoint.sh"]
CMD ["nginx", "-g", "daemon off;"]