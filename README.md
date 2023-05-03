Download Link: https://assignmentchef.com/product/solved-cs307-assignment1-database-design
<br>
As we know, the China’s rail network is complex, more than 5000 station distribute in 657 citys and connected by 140000km railway. There are so many passengers take the train each day and processing these informations is a real challeng. You, a SUSTech student who want to improve the experience of 12306 and refactor their database.

<h1>BEFORE START</h1>

Although there are standards, database designing is still a highly subjective intellectual activity. As graders, we will set some rules for grading, but as long as your design can satisfy our requirements, you should be able to get the points.

Since table name and field name is case-insensitive, it is recommended to use underline “_” to separate words, instead of using camel naming.(e.g. <sub>Use my_great_table</sub> ,

some_informative_field instead of MyGreateTable or SomeInformativeField .)

Example fields are only for reference. You may create new fields and combine/separate these fields to simplify your design, but the information needs to be remained at least.

<h1>DETAILS ABOUT THE RELATIONSHIPS</h1>

Store data about rail lines and rail station in an organized and easy-to-maintain manner (see the keywords below).

City and Station

A city have multiple rail stations A city can have no stations A station must be in a city. Train and Seat

Different trains have different seat count and different seat type.

Price of different seat type in the same train is different and the number of remaining tickets should be calculated dynamically. Ticket

A concrete train in concrete date. For example, “G74” in Feb. 28th or Feb. 29th.

Needs arrive station and depart station, and their datetime. Need seat type… or other you think is necessary

The user must record it’s ID card, the ID card number may have a ‘x’ in its last digit. Needs phone number Order

The Order should record user, create date, order status, train num, the depart city, arrive city and price, etc. Other General Requirement:

The passengers can get on or get off the train in each station where the train will stop.

The ticket should be allocated to the city not the train, for example, there is a train from

Shenzhen to Guangzhou, which will stop 10 min at Dongguan, the left tickets from

Dongguan to Guangzhou should be larger than the left tickets from Shenzhen to Guangzhou.

In each train, such as “G74”, we can find all passing stations in it, and for one station in this train, we can find its former and next station from your design. For example, the former station of “WU HAN” in “G74” is “YUE YAND DONG”.

From your design, we can easily get all information as the graph below

Design a database allowing to manage all information mentioned above in this document, and contains all fields in the table below.

Your design needs to follow the requirements of the three normal forms

Use primary key and foreign keys to indicate important attributes and relationships about your data

Every row in each table should to be uniquely identified by its primary key.(You may use simple or composite primary key).

Every table should be involved in a link. No isolate tables included.

(ํᘏ౲҅Ძक़ํᥝᤒӻྯٌ՜ᤒጱक़Ძ೰ݻ)

Your design should contain no circular links

ොᲫक़ጱᳵԏᤒԭ੒ҁݻ҅ӧᚆํሾ҂

Each table should always have at least one mandatory (“Not Null”) column(including the primary key but not the id column)

Table with only one column is not allowed(Not include the id column).

ࣁਂᚆӧҁݝํӞڜጱᤒ҅ӧ۱ތԆᲫid҂

Tables with no other unique columns than possibly a system-generated ID is not allowed. ҁᴻԧԆᲫᛔीጱidํᥝᵱ҅क़ԏٌ՜uniqueጱ๳ᕅڜ҂

Use appropriate types for different fields of data

You need to use relative regular name format so that we can understand it easily. For instance, you need to use the field names mentioned in the table below unless you decide to split or merge them. The names of relationship tables need to reflect the related entities, etc               Arrange your model diagram in a way that helps understanding your design.

<strong>Fields must contain</strong>

<table width="629">

 <tbody>

  <tr>

   <td width="129"><strong>Field</strong></td>

   <td width="282"><strong>Explanation</strong></td>

   <td width="219"><strong>Example</strong></td>

  </tr>

  <tr>

   <td width="129">city_name</td>

   <td width="282">Name of city</td>

   <td width="219">Shenzhen, Beijing</td>

  </tr>

  <tr>

   <td width="129">station_name</td>

   <td width="282">Name of rail station</td>

   <td width="219">Shenzhen North station</td>

  </tr>

  <tr>

   <td width="129">depart_time</td>

   <td width="282">Time to leave the station(For each station)</td>

   <td width="219">2020.02.29-18:00:21</td>

  </tr>

  <tr>

   <td width="129">arrive_time</td>

   <td width="282">Time that will arrive the station(For each station)</td>

   <td width="219">2020.02.29-18:00:21</td>

  </tr>

  <tr>

   <td width="129">depart_station</td>

   <td width="282">The start station of the train</td>

   <td width="219">Shenzhen North station</td>

  </tr>

  <tr>

   <td width="129">arrive_station</td>

   <td width="282">The destination station of the train</td>

   <td width="219">Shenzhen North station</td>

  </tr>

  <tr>

   <td width="129">ticket_entrance</td>

   <td width="282">The ticket entrance is where to check your ticket</td>

   <td width="219">2A, 3B, 16A</td>

  </tr>

  <tr>

   <td width="129">seat_type</td>

   <td width="282">The type of the seat</td>

   <td width="219">Hard seat, Soft sleeper</td>

  </tr>

  <tr>

   <td width="129">rest_ticket</td>

   <td width="282">The rest of the ticket</td>

   <td width="219">32</td>

  </tr>

  <tr>

   <td width="129">ticket_price</td>

   <td width="282">The Price of the ticket</td>

   <td width="219">1145.14</td>

  </tr>

  <tr>

   <td width="129">create_date</td>

   <td width="282">The date that create the order</td>

   <td width="219">2020.02.29-18:00:21</td>

  </tr>

  <tr>

   <td width="129">order_status</td>

   <td width="282">The status of the order</td>

   <td width="219">0, 1, 2(correspond to multiple states)</td>

  </tr>

  <tr>

   <td width="129">order_price</td>

   <td width="282">The price of the order</td>

   <td width="219">1145.14</td>

  </tr>

  <tr>

   <td width="129">username</td>

   <td width="282">Name of the user</td>

   <td width="219">Shiyi Chen, Xin Yao</td>

  </tr>

  <tr>

   <td width="129">phone_number</td>

   <td width="282">phone number of user</td>

   <td width="219">13899998888</td>

  </tr>

  <tr>

   <td width="129">ID_card_num</td>

   <td width="282">The ID card number of user</td>

   <td width="219">11111120000229111x</td>

  </tr>

 </tbody>

</table>

Submission