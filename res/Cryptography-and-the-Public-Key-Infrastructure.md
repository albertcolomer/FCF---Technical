
# Module 1: Cryptography and the Public Key Infrastructure
   - [Ciphers Lesson](#Ciphers-Lesson)
   - [Keys and Cryptographic Algorithms Lesson](#Keys-and-Cryptographic-Algorithms-Lesson)
   - [Hashing and Digital Signatures](#Hashing-and-Digital-Signatures)
   - [Public Key Infrastructure](#Public-Key-Infrastructure)


<br>

<br>

## Cryptography and the Public Key Infrastructure Overview

La tecnología criptográfica permite cifrar datos y firmarlos digitalmente. El cifrado es el proceso de
convertir texto plano en texto criptográfico, es decir, hacer ilegible algo que era legible. Una firma
también utiliza la criptografía para producir un valor único que puede vincularse a una persona. En la mayoría de las jurisdicciones, una
firma digital es legalmente equivalente a una firma manuscrita.
El cifrado y el uso de una firma digital satisfacen una serie de objetivos. Por ejemplo, el cifrado garantiza que
confidencialidad de la información. La firma digital garantiza la integridad y autenticidad de los datos.
datos. Puede utilizarse para identificar o autenticar una entidad. También puede garantizar el no repudio. El no repudio tiene
implicaciones legales y significa que el firmante no puede negar haber firmado la información. Si la información es un
Si la información es un contrato legal, el firmante está vinculado al contrato por su firma digital.
Al satisfacer estos cuatro términos -confidencialidad, integridad de los datos, autenticación y no repudio- la criptografía
ha facilitado el auge del comercio electrónico y las comunicaciones seguras.
En este módulo aprenderás sobre cifrado, claves digitales y certificados, algoritmos criptográficos, funciones hash, la firma digital y el cifrado.
los procesos de firma digital y cifrado, y la PKI. Una vez completado este módulo, tendrá una
Una vez finalizado este módulo, comprenderás mejor el funcionamiento de estas tecnologías y tendrás una idea más clara de cómo han hecho posible el comercio electrónico y las comunicaciones seguras.

<br>

<br>

## Ciphers Lesson

La potencia de los ordenadores permite un cifrado más sofisticado, pero los conceptos siguen siendo los mismos. Dos
tipos de cifrado que se emplean habitualmente son los de flujo y los de bloque.
Los cifradores de flujo cifran un flujo de datos de texto sin formato, bit a bit o byte a byte. Ejemplos de cifradores de flujo son `FISH`
y RC4. Son más rápidos que los de bloque.
Los cifradores de bloques dividen el texto plano en bloques para cifrarlo. El tamaño de los bloques viene determinado por el tamaño de la clave.
clave. Si la clave es de 256 bits, los bloques a cifrar también serán de 256 bits. Si el tamaño del mensaje es de un
megabyte, el mensaje se dividirá en varios bloques de 256 bits cada uno.
Los cifradores por bloques más comunes hoy en día son `Data Encryption Standard (DES)`, `3DES`, `Advanced Encryption
(AES) y Blowfish`.

<br>

## Keys and Cryptographic Algorithms Lesson

¿Qué es una clave digital?
En lo que respecta al cifrado, las claves pueden utilizarse para cifrar el flujo de información entre dos dispositivos, un volumen
o un pequeño fragmento de datos, como otra clave digital o un valor hash de salida.
Dependiendo de la tarea que realice la clave, su vida útil puede ser de años o de unos segundos. Por ejemplo, una clave
Por ejemplo, una clave utilizada para firmar certificados puede ser válida durante diez o más años, pero una clave utilizada para cifrar una sesión entre dos dispositivos sólo se utiliza durante el tiempo que dura la sesión.
dispositivos sólo se utiliza mientras dura esa sesión.
Las claves suelen ser privadas o secretas, pero también pueden ser públicas. Las claves públicas suelen escribirse en los
certificados

Las claves públicas suelen ser de 1024 bits, 2048 bits o más. se utilizan a menudo para cifrar pequeños fragmentos de datos, como otra clave o
un hash de datos. 
Las claves más pequeñas, de entre 128 y 256 bits, se utilizan para cifrar grandes cantidades de datos.
La complejidad de la clave también es un factor importante.
Una sal es un valor aleatorio que se añade a otro valor para aumentar la entropía.
BCRYPT es el algoritmo por defecto utilizado para el estiramiento de claves en OpenBSD y varias distribuciones de Linux, una contraseña se convierte en hash varias veces antes de añadirle una sal de 128 bits.

Un algoritmo simétrico es un cifrado utilizado para cifrar y descifrar datos utilizando la misma clave. data encryption standard (DES), 3DES, International Encryption Algorithm (IDEA), Advanced Encryption Standard (AES), Rivesst Cipher (RC$, RC5, RC6) A excepción del RC4, que es un cifrado de flujo, el resto son cifrados de bloque. blowfish/Twofish
Un algoritmo asimétrico es un cifrado utilizado para realizar operaciones criptográficas utilizando un par de claves relacionadas matemáticamente. permite a dos partes intercambiar de forma segura un secreto, o clave, a través de un canal público Diffie-Hellman, Rivest, Shamir and Adleman (RSA) Eliptic Curve Crytography (ECC) Prety Good Privacy (PGP) and GPG, Digital Signing Algorithm (DSA)

<br>

## Hashing and Digital Signatures

El hashing es el proceso de convertir datos de tamaño arbitrario en un valor único de tamaño fijo, características importantes que soportan la criptografía:
- El valor de salida tiene una longitud fija, no hay información sobre el tamaño de los datos de entrada.
- El valor de salida es único para cada valor de entrada
- No es reversible o sólo va en una dirección

Combinando las características de seguridad del hash con la criptografía asimétrica se puede obtener una firma digital.<br>
Las firmas digitales garantizan 
- la integridad de los datos de la información firmada
- autentican a la persona o cosa que firmó la información 
- permiten el no repudio 

Proceso:
- Se realiza un hash de la información que debe firmarse
- Se cifra el valor de salida mediante un algoritmo asimétrico, denominado firma digital. las claves públicas se escriben en certificados emitidos por autoridad de certificación (CA)
- Se adjunta la firma digital a la información

Funciones hash más comunes:
-  MD5, salida hash de 128 bits, debilidades, principalmente la susceptibilidad a las colisiones.
- MD6, 
- SHA-1, produce un hash de 160 bits
- SHA-2, es un conjunto de algoritmos hash (SHA-224, SHA-256, SHA-384
y SHA-512)
- SHA-3 permite decidir la longitud del valor de salida.
- LANMAN, utiliza el estándar
(DES)
- NTLM, NTLM v2
- HAVAL y RIPEMD

Cuando el hash se utiliza para proteger contraseñas, se puede aumentar la entropía mediante el proceso de estiramiento de claves.

<br>

## Public Key Infrastructure

En criptografía, un certificado digital es un documento electrónico, emitido y firmado por una entidad de confianza, como una CA.
Contiene el nombre del titular del certificado y puede o no contener una clave pública. Si el certificado se emite para
Si el certificado se expide a una persona, dispositivo o aplicación concretos, vincula la identidad de la entidad a la clave pública mediante una firma digital.

Las listas de revocación de certificados (CRL) son certificados que contienen información sobre certificados en los que ya no se confía. Emitido por Authority revocation list (ARL)

Existen diferentes estándares y mejores prácticas para la producción y gestión de certificados, el más importante es X.509 versión 3. 

La CA realiza dos funciones:
- Emite certificados a entidades finales, como personas y dispositivos
- Emite certificados para ayudar a gestionar los certificados de las entidades finales

las CA múltiples pueden organizarse de diferentes maneras:
- Entorno jerárquico, habría una CA raíz (es la fuente de confianza) y una o más CA subordinadas(emiten certificados a las entidades finales)
- Estructura lateral, una CA de una PKI confíe en una CA de otra PKI mediante certificación cruzada

La cadena de confianza es una serie de certificados asociados, cada uno de los cuales depende del otro para confiar.

protocolo ligero de acceso a directorios (LDAP)
La RA verifica y envía las solicitudes de certificados a la CA. registra las solicitudes aprobadas con la CA, que genera y proporciona un código de autorización de un solo uso al solicitante

solicitud de servicio de certificado (CSR)
proveedor de servicios criptográficos (CSP) de Microsoft.


<br>
