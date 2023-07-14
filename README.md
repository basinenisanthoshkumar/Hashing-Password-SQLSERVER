# Hashing-Password-SQLSERVER
This repo is for conversion of string to hash code while storing in database.


DECLARE @BinaryData VARBINARY(20) = 0x48656C6C6F20576F726C64; -- Binary representation of "Hello World"

SELECT 
    CONVERT(VARCHAR(100), @BinaryData, 0) AS BinaryFormat,
    CONVERT(VARCHAR(100), @BinaryData, 1) AS HexadecimalFormat,
    CONVERT(VARCHAR(100), @BinaryData, 120) AS Base64Format,
    CONVERT(VARCHAR(100), @BinaryData, 121) AS UrlSafeBase64Format;


BinaryFormat         HexadecimalFormat    Base64Format    UrlSafeBase64Format
-------------------- -------------------- --------------- --------------------
Hello World          0x48656C6C6F20576F726C64   SGVsbG8gV29ybGQ=   SGVsbG8gV29ybGQ=
