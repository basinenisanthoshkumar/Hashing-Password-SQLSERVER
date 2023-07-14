# Hashing-Password-SQLSERVER
This repo is for conversion of string to hash code while storing in database.


DECLARE @BinaryData VARBINARY(20) = 0x48656C6C6F20576F726C64; -- Binary representation of "Hello World"

SELECT 
    CONVERT(VARCHAR(100), @BinaryData, 0) AS BinaryFormat,
    CONVERT(VARCHAR(100), @BinaryData, 1) AS HexadecimalFormat,
    CONVERT(VARCHAR(100), @BinaryData, 2) AS HexadecimalFormat, 
    CONVERT(VARCHAR(100), @BinaryData, 120) AS Base64Format,
    CONVERT(VARCHAR(100), @BinaryData, 121) AS UrlSafeBase64Format;


BinaryFormat  =   Hello World     

(1)HexadecimalFormat = 0x48656C6C6F20576F726C64  
Format code 1 (1) represents the conversion of binary data to a hexadecimal string with a leading 0x prefix. This format is commonly used when you want to represent binary data as a hexadecimal value.

(2)HexadecimalFormat = 48656C6C6F20576F726C64 
Format code 2 (2) represents the conversion of binary data to a hexadecimal string without the leading 0x prefix. It is similar to format code 1, but it excludes the prefix.

Base64Format   = SGVsbG8gV29ybGQ= 

UrlSafeBase64Format =  SGVsbG8gV29ybGQ=
