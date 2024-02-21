FROM mcr.microsoft.com/dotnet/sdk:7.0
LABEL author="Ashfaque" project="NopCommerce"
ENV ASPNETCORE_URLS="http://0.0.0.0:5000"
COPY nopcommerce /nopcommerce
RUN adduser -h /nopcommerce -s /bin/bash -D nop && chown -R nop:nop /nopcommerce
USER nop
WORKDIR /nopcommerce
EXPOSE 5000
CMD [ "dotnet","Nop.Web.dll" ]