Download Link: https://assignmentchef.com/product/solved-cs6360-001-assignment-5
<br>
<strong>Database Design </strong>

<strong> </strong>




<strong> </strong>

<ol>

 <li>Consider a disk with block size B=512 bytes. A block pointer is P=6 bytes long,</li>

</ol>

and a record pointer is P R =7 bytes long. A file has r=3000 EMPLOYEE records

of fixed-length. Each record has the following fields: NAME (30 bytes), SSN (10

bytes), DEPARTMENTCODE (10 bytes), ADDRESS (30 bytes), PHONE (10 bytes),

BIRTHDATE (10 bytes), GENDER (1 byte), JOBCODE (4 bytes), SALARY (4 bytes, real

number). An additional byte is used as a deletion marker.




<strong>(60 points)</strong>




(a) Calculate the record size R in bytes.




(b) Calculate the blocking factor bfr and the number of file blocks b assuming an

unspanned organization.




(c) Suppose the file is ordered by the key field SSN and we want to construct a primary index on SSN. Calculate (i) the index blocking factor bfr i; (ii) the number of first-level index entries and the number of first-level index blocks; (iii) the number of levels needed if we make it into a multi-level index; (iv) the total number of blocks required by the multi-level index; and (v) the number of block accesses needed to search for and retrieve a record from the file–given its SSN value–using the primary index.




(d) Suppose the file is not ordered by the key field SSN and we want to construct a

secondary index on SSN. Repeat the previous exercise (part c) for the secondary

index and compare with the primary index.




(e) Suppose the file is not ordered by the non-key field DEPARTMENTCODE and we want to construct a secondary index on DEPARTMENTCODE using Option 3 of Section 18.1.3, with an extra level of indirection that stores record pointers. Assume there are 100 distinct values of DEPARTMENTCODE, and that the EMPLOYEE records are evenly distributed among these values. Calculate (i) the index blocking factor bfr i;

(ii) the number of blocks needed by the level of indirection that stores record pointers; (iii) the number of first-level index entries and the number of first-level index blocks; (iv) the number of levels needed if we make it a multi-level index; (v) the total number of blocks required by the multi-level index and the blocks used in the extra level of indirection; and (vi) the approximate number of block accesses needed to search for and retrieve all records in the file having a specific DEPARTMENTCODE value using the index.




(f) Suppose the file is ordered by the non-key field DEPARTMENTCODE and we want to construct a clustering index on DEPARTMENTCODE that uses block anchors (every new value of DEPARTMENTCODE starts at the beginning of a new block). Assume there are 100 distinct values of DEPARTMENTCODE, and that the EMPLOYEE records are evenly distributed among these values. Calculate (i) the index blocking factor bfr i; (ii) the number of first-level index entries and the number of first-level index blocks; (iii) the number of levels needed if we make it a multi-level index; (iv) the total number of blocks required by the multi-level index; and (v) the number of block accesses needed to search for and retrieve all records in the file having a specific DEPARTMENTCODE value using the clustering index (assume that multiple blocks in a cluster are either contiguous or linked by pointers).







(g) Suppose the file is not ordered by the key field Ssn and we want to construct a B+ tree access structure (index) on SSN. Calculate (i) the orders p and p leaf of the

B+ tree; (ii) the number of leaf-level blocks needed if blocks are approximately

69% full (rounded up for convenience); (iii) the number of levels needed if internal nodes are also 69% full (rounded up for convenience); (iv) the total number of blocks required by the B+ tree; and (v) the number of block accesses needed to search for and retrieve a record from the file –given its SSN value– using the B+ tree.







<ol start="2">

 <li>A PARTS file with Part# as key field includes records with the following Part# values: 23, 65, 37, 60, 46, 92, 48, 71, 56, 59, 18, 21, 10, 74, 78, 15, 16, 20, 24, 28, 39, 43, 47, 50, 69, 75, 8, 49, 33, 38. Suppose the search field values are inserted in the given order in a B+ tree of order p=4 and p-leaf =4; show the final tree.</li>

</ol>




<ol start="3">

 <li>Which of the following schedules is (conflict) serializable? For each serializable schedule, determine the equivalent serial schedules.</li>

</ol>




(a) r1 (X); r3 (X); w1(X); r2(X); w3(X)




(b) r1 (X); r3 (X); w3(X); w1(X); r2(X)




(c) r3 (X); r2 (X); w3(X); r1(X); w1(X)




(d) r3 (X); r2 (X); r1(X); w3(X); w1(X)































<ol start="4">

 <li>Consider the three transactions T1, T2, and T3, and the schedules S1 and S2 given below. Draw the serializibility (precedence) graphs for S1 and S2 and state whether each schedule is serializable or not. If a schedule is serializable, write down the equivalent serial schedule(s).</li>

</ol>




T1: r1(x); r1(z); w1(x)

T2: r2(z); r2(y); w2(z); w2(y)

T3: r3(x); r3(y); w3(y)




S1: r1(x); r2(z); r1(z); r3(x); r3(y); w1(x); w3(y); r2(y); w2(z); w2(y)

S2: r1(x); r2(z); r3(x); r1(z); r2(y); r3(y); w1(x); w2(z); w3(y); w2(y)




<strong> </strong>

<ol start="5">

 <li>Explain ACID properties of transaction processing systems. What is the protocol that ensures isolation in addition to serializability.</li>

</ol>

<strong> </strong>

All questions except question #1 are <strong>10 points.</strong>

<strong> </strong>


