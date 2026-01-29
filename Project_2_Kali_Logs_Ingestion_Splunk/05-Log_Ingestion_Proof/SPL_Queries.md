🖼️ **Screenshot 1 — Index Has Events**



Filename:

01\_Log\_Ingestion\_Index\_Proof.png



**SPL Query:**

**index=linux**



-------------------------------------------------------------------------------------------------------------------------



🖼️ **Screenshot 2 — Host Sending Logs**



Filename:

02\_Log\_Ingestion\_Host\_Proof.png



**SPL Query:**

**index=linux**

**| stats count by host**



---------------------------------------------------------------------------------------------------------------------------



🖼️ **Screenshot 3 — Source File Proof**



Filename:

03\_Log\_Ingestion\_Source\_Proof.png



**SPL Query:**

**index=linux**

**| stats count by source**





-----------------------------------------------------------------------------------------------------------------------------

🖼️ **Screenshot 4 — Forwarder Activity**



Filename:

04\_Log\_Ingestion\_Forwarder\_Proof.png



**SPL Query:**

**index=\_internal sourcetype=splunkd component=TcpOutputProc**



------------------------------------------------------------------------------------------------------------------------------



🖼️ **Screenshot 5 — Timeline Continuity**



Filename:

05\_Log\_Ingestion\_Timeline.png



**SPL Query:**

**index=linux**

**| timechart count**



**------------------------------------------------------------------------------------------------------------------------------**



