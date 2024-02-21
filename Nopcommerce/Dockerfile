FROM mcr.microsoft.com/dotnet/sdk:7.0
LABEL author="Ashfaque" project="nopcommerce"
RUN mkdir /nopcommerce
COPY nopcommerce /nopcommerce
EXPOSE 5000
WORKDIR /nopcommerce
CMD [ "dotnet","Nop.Web.dll","--urls="http:/0.0.0.0/5000"" ]