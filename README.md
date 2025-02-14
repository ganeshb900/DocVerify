# DocVerify
DocVerify: A RESTful application for signing and verifying documents using digital signatures. It provides endpoints to generate public keys, sign documents, and verify the authenticity of documents by checking if they have been tampered with. Secure, efficient, and easy to use for ensuring document integrity
1) getting pulic key
curl --location 'localhost:8080/api/public-key'

2      create Signiture of the file 
curl --location 'http://localhost:8080/api/sign' \
--form 'file=@"/C:/Users/ganesh.borde/Downloads/Payslip for January-2025-554.pdf"'


3   match / verify the signature 
curl --location 'http://localhost:8080/api/verify' \
--form 'file=@"/C:/Users/ganesh.borde/Downloads/Payslip for January-2025-554.pdf"' \
--form 'signature="N+MhdTAhuNrC/1VYLocUyHKdAljcbFmzNMtg4ULDVAUxpa5qhCgKSwhl0K1W8x2H157UkPMB0PsTNUZxN8iM4Bd9yibuOS8KKyz++pDnzmSVGTLRWKHmK63S/efoWf7Zvuh1p73e3gWTbB8/OU4xPvc6WE0vRWSqHLKPtfZFUW5OSuexnz3VA+ucO+dvqAetOQDOX3nSbsEm4wpzU66z/tu7YtO9TuGppCjuIPL4yxDYzBFW/9kKBXRdYJ+7EiYDZfjzVf5bDNbUMACI2/dz6uE3IYaW/+Mrpzc6FXdfvq/PvLBzgtNgt0NJcwt+khR3L2ve5WrtvRlDCzU3L2jGiQ=="'





