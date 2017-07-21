---
- config:
    - testset: "TACKO API Tests"

- test: # login app use method POST
    - name: "Login app with valid info"
    - url: "/api/auth/signIn"
    - method: "POST"
    - headers: {'Content-Type': 'application/json'}
    - body: '{"username": "bich.pham@beesightsoft.com",
              "password": "123456",
              "grant_type": "password",
              "client_id": "2",
              "client_secret": "fOtoyx3BAzoKHjWRpwng4CPxQd1zYz88WiAZUlhW",
              "email": "bich.pham@beesightsoft.com",
              "device_platform": "ios",
              "device_token": "a437dd18254449779569cc1322a87791a426ad0c3e33aaf92379fac65d89758e",
              "longitude": "106.66033",
              "latitude": "10.7919413"}'   
    - expected_status: [200]
    - validators:
        - compare: {jsonpath_mini: 'data.email', comparator: 'str_eq', expected: "bich.pham@beesightsoft.com"}
        - compare: {jsonpath_mini: 'data.username', comparator: 'str_eq', expected: "Pham Ngoc Bich"}