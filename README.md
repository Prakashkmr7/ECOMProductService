[19/10/23 - Building APIs - 2] -> Call to FakeStore using RestTemplate to get a single product
1. Created the models
2. Created the required DTOs
3. Created the controller
4. Created the service layer
5. Implemented RestTemplate
6. Invoked call to 3rd party [ FakeStoreAPI ] to get data
7. Returned response from controller

Url of FakeStore-
https://fakestoreapi.com/docs

[23/10/23 - Building APIs - 3] -> CRUD APIs, Exception Handling
1. Constructor Injection
2. 5 CRUD APIs - getProduct(id), getAllProducts(), createProduct()
3. Updated the service layer for new APIs
4. Wrote a small intro to Controller Advice



Controller -> RequestDTO, ResponseDTO
CreateProductRequestDTO, -> has all attributes except "id"
ProductResponseDTO -> has all the attributes
--------------------------------------------------------------------------------
Client -> RequestDTO, ResponseDTO
FakeStoreCreateProductRequestDTO -> has all attributes except "id"
FakeStoreProductResponseDTO -> has all the attributes


Youtube

user uploads a video -> VideoIngestionService -> VideoStore

VideoUploadRequestDTO : controller -> VideoIngestionService
    name
    description
    thumbnail
    bookmarks
    videoFile
    format
    uploadedAt
    uploadedBy

VideoStoreCreateVideoRequestDTO : VideoStoreClient -> VideoIngestionService
    name
    description
    thumbnail
    bookmarks
    videoFile
    format
    uploadedAt
    uploadedBy
    tags
    topics
    constant for algo
    List<Resolutions>




VideoIngestionService

VideoStore -> only to store the videos : platform DB

Calling any 3rd party

Repo -> Service -> Controller
Client -> Service -> Controller

Development Cycle -> local, dev[dev instances], UAT/QA/staging[prod replica], prod
UAT -> User Acceptance Testing



Configuration Details -
ddl.auto -> create, update, verify
Create : everytime you start the application, it will drop all the tables and recreate them. High chances of losing data.
Update : everyime you start the application, only the update changes are implemented.
Verify : it does not create/udpate anything, it just verifies if the DB has all the tables/columns/mappings as mentioned in the entities. -> Generally used in companies, for production

Local development -> create or update
Production -> verify [ generally tables via separate scripts like FlyWay, Liquibase ]





Reading Content URL :-
UUID - https://uuid.ramsey.dev/en/stable/rfc4122/version7.html
https://en.wikipedia.org/wiki/Universally_unique_identifier
Hibernate Content - https://hibernate.org/orm/
