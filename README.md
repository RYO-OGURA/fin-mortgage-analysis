# fin-mortgage-analysis
code for mortgage credit risk


  /* 
	Ryo Ogura
    USE mysql;



*/

/****** Object:  Database [FinancialData]    Script Date: ******/

create database credit;

use credit;
show variables like 'innodb_file_per_table';

CREATE TABLE origin
(
	score int(3),
	fpmtdate int(6),
	f_t char(1),
	m_date int(6),
	msa_md DECIMAL(7,2),
	mi decimal(4,1),
	unit int(1),
	occ char(1),
	cltv decimal(8,4),
	dti int(3),
	upb int(12),
	ltv int(3),
	i_rate decimal(6,3),
	channel char(1),
	ppm char(1),
	p_type char(5),
	pro_state char(2),
	pro_type char(2),
	postal int(5),
	loan_seq_no char(12),
	purpose char(1),
	l_term int(3),
	n_of_borrowers int(2),
	seller_name varchar(20),
	service_name varchar(20),
	PRIMARY KEY(loan_seq_no)
) DATA directory = 'H:/mysql';

/* Origin data load */
LOAD DATA CONCURRENT LOCAL INFILE 'C:/rawdata/originQ11999.txt'
    IGNORE
    INTO TABLE origin
    CHARACTER SET default
    FIELDS
        TERMINATED BY '|'
    LINES
        STARTING BY ''
        TERMINATED BY '\n'
	(score,
	fpmtdate,
	f_t,
	m_date,
	msa_md,
	mi,
	unit,
	occ,
	cltv,
	dti,
	upb,
	ltv,
	i_rate,
	channel,
	ppm,
	p_type,
	pro_state,
	pro_type,
	postal,
	loan_seq_no,
	purpose,
	l_term,
	n_of_borrowers,
	seller_name,
	service_name);
    
LOAD DATA CONCURRENT LOCAL INFILE 'C:/rawdata/originQ21999.txt'
    IGNORE
    INTO TABLE origin
    CHARACTER SET default
    FIELDS
        TERMINATED BY '|'
    LINES
        STARTING BY ''
        TERMINATED BY '\n'
	(score,
	fpmtdate,
	f_t,
	m_date,
	msa_md,
	mi,
	unit,
	occ,
	cltv,
	dti,
	upb,
	ltv,
	i_rate,
	channel,
	ppm,
	p_type,
	pro_state,
	pro_type,
	postal,
	loan_seq_no,
	purpose,
	l_term,
	n_of_borrowers,
	seller_name,
	service_name);
    
LOAD DATA CONCURRENT LOCAL INFILE 'C:/rawdata/originQ31999.txt'
    IGNORE
    INTO TABLE origin
    CHARACTER SET default
    FIELDS
        TERMINATED BY '|'
    LINES
        STARTING BY ''
        TERMINATED BY '\n'
	(score,
	fpmtdate,
	f_t,
	m_date,
	msa_md,
	mi,
	unit,
	occ,
	cltv,
	dti,
	upb,
	ltv,
	i_rate,
	channel,
	ppm,
	p_type,
	pro_state,
	pro_type,
	postal,
	loan_seq_no,
	purpose,
	l_term,
	n_of_borrowers,
	seller_name,
	service_name);
LOAD DATA CONCURRENT LOCAL INFILE 'C:/rawdata/originQ41999.txt'
    IGNORE
    INTO TABLE origin
    CHARACTER SET default
    FIELDS
        TERMINATED BY '|'
    LINES
        STARTING BY ''
        TERMINATED BY '\n'
	(score,
	fpmtdate,
	f_t,
	m_date,
	msa_md,
	mi,
	unit,
	occ,
	cltv,
	dti,
	upb,
	ltv,
	i_rate,
	channel,
	ppm,
	p_type,
	pro_state,
	pro_type,
	postal,
	loan_seq_no,
	purpose,
	l_term,
	n_of_borrowers,
	seller_name,
	service_name);
LOAD DATA CONCURRENT LOCAL INFILE 'C:/rawdata/originQ12000.txt'
    IGNORE
    INTO TABLE origin
    CHARACTER SET default
    FIELDS
        TERMINATED BY '|'
    LINES
        STARTING BY ''
        TERMINATED BY '\n'
	(score,
	fpmtdate,
	f_t,
	m_date,
	msa_md,
	mi,
	unit,
	occ,
	cltv,
	dti,
	upb,
	ltv,
	i_rate,
	channel,
	ppm,
	p_type,
	pro_state,
	pro_type,
	postal,
	loan_seq_no,
	purpose,
	l_term,
	n_of_borrowers,
	seller_name,
	service_name);
LOAD DATA CONCURRENT LOCAL INFILE 'C:/rawdata/originQ22000.txt'
    IGNORE
    INTO TABLE origin
    CHARACTER SET default
    FIELDS
        TERMINATED BY '|'
    LINES
        STARTING BY ''
        TERMINATED BY '\n'
	(score,
	fpmtdate,
	f_t,
	m_date,
	msa_md,
	mi,
	unit,
	occ,
	cltv,
	dti,
	upb,
	ltv,
	i_rate,
	channel,
	ppm,
	p_type,
	pro_state,
	pro_type,
	postal,
	loan_seq_no,
	purpose,
	l_term,
	n_of_borrowers,
	seller_name,
	service_name);
LOAD DATA CONCURRENT LOCAL INFILE 'C:/rawdata/originQ32000.txt'
    IGNORE
    INTO TABLE origin
    CHARACTER SET default
    FIELDS
        TERMINATED BY '|'
    LINES
        STARTING BY ''
        TERMINATED BY '\n'
	(score,
	fpmtdate,
	f_t,
	m_date,
	msa_md,
	mi,
	unit,
	occ,
	cltv,
	dti,
	upb,
	ltv,
	i_rate,
	channel,
	ppm,
	p_type,
	pro_state,
	pro_type,
	postal,
	loan_seq_no,
	purpose,
	l_term,
	n_of_borrowers,
	seller_name,
	service_name);
    
LOAD DATA CONCURRENT LOCAL INFILE 'C:/rawdata/originQ42000.txt'
    IGNORE
    INTO TABLE origin
    CHARACTER SET default
    FIELDS
        TERMINATED BY '|'
    LINES
        STARTING BY ''
        TERMINATED BY '\n'
	(score,
	fpmtdate,
	f_t,
	m_date,
	msa_md,
	mi,
	unit,
	occ,
	cltv,
	dti,
	upb,
	ltv,
	i_rate,
	channel,
	ppm,
	p_type,
	pro_state,
	pro_type,
	postal,
	loan_seq_no,
	purpose,
	l_term,
	n_of_borrowers,
	seller_name,
	service_name);
    

LOAD DATA CONCURRENT LOCAL INFILE 'C:/rawdata/originQ12001.txt'
    IGNORE
    INTO TABLE origin
    CHARACTER SET default
    FIELDS
        TERMINATED BY '|'
    LINES
        STARTING BY ''
        TERMINATED BY '\n'
	(score,
	fpmtdate,
	f_t,
	m_date,
	msa_md,
	mi,
	unit,
	occ,
	cltv,
	dti,
	upb,
	ltv,
	i_rate,
	channel,
	ppm,
	p_type,
	pro_state,
	pro_type,
	postal,
	loan_seq_no,
	purpose,
	l_term,
	n_of_borrowers,
	seller_name,
	service_name);
LOAD DATA CONCURRENT LOCAL INFILE 'C:/rawdata/originQ22001.txt'
    IGNORE
    INTO TABLE origin
    CHARACTER SET default
    FIELDS
        TERMINATED BY '|'
    LINES
        STARTING BY ''
        TERMINATED BY '\n'
	(score,
	fpmtdate,
	f_t,
	m_date,
	msa_md,
	mi,
	unit,
	occ,
	cltv,
	dti,
	upb,
	ltv,
	i_rate,
	channel,
	ppm,
	p_type,
	pro_state,
	pro_type,
	postal,
	loan_seq_no,
	purpose,
	l_term,
	n_of_borrowers,
	seller_name,
	service_name);
LOAD DATA CONCURRENT LOCAL INFILE 'C:/rawdata/originQ32001.txt'
    IGNORE
    INTO TABLE origin
    CHARACTER SET default
    FIELDS
        TERMINATED BY '|'
    LINES
        STARTING BY ''
        TERMINATED BY '\n'
	(score,
	fpmtdate,
	f_t,
	m_date,
	msa_md,
	mi,
	unit,
	occ,
	cltv,
	dti,
	upb,
	ltv,
	i_rate,
	channel,
	ppm,
	p_type,
	pro_state,
	pro_type,
	postal,
	loan_seq_no,
	purpose,
	l_term,
	n_of_borrowers,
	seller_name,
	service_name);
LOAD DATA CONCURRENT LOCAL INFILE 'C:/rawdata/originQ42001.txt'
    IGNORE
    INTO TABLE origin
    CHARACTER SET default
    FIELDS
        TERMINATED BY '|'
    LINES
        STARTING BY ''
        TERMINATED BY '\n'
	(score,
	fpmtdate,
	f_t,
	m_date,
	msa_md,
	mi,
	unit,
	occ,
	cltv,
	dti,
	upb,
	ltv,
	i_rate,
	channel,
	ppm,
	p_type,
	pro_state,
	pro_type,
	postal,
	loan_seq_no,
	purpose,
	l_term,
	n_of_borrowers,
	seller_name,
	service_name);
LOAD DATA CONCURRENT LOCAL INFILE 'C:/rawdata/originQ12002.txt'
    IGNORE
    INTO TABLE origin
    CHARACTER SET default
    FIELDS
        TERMINATED BY '|'
    LINES
        STARTING BY ''
        TERMINATED BY '\n'
	(score,
	fpmtdate,
	f_t,
	m_date,
	msa_md,
	mi,
	unit,
	occ,
	cltv,
	dti,
	upb,
	ltv,
	i_rate,
	channel,
	ppm,
	p_type,
	pro_state,
	pro_type,
	postal,
	loan_seq_no,
	purpose,
	l_term,
	n_of_borrowers,
	seller_name,
	service_name);
LOAD DATA CONCURRENT LOCAL INFILE 'C:/rawdata/originQ22002.txt'
    IGNORE
    INTO TABLE origin
    CHARACTER SET default
    FIELDS
        TERMINATED BY '|'
    LINES
        STARTING BY ''
        TERMINATED BY '\n'
	(score,
	fpmtdate,
	f_t,
	m_date,
	msa_md,
	mi,
	unit,
	occ,
	cltv,
	dti,
	upb,
	ltv,
	i_rate,
	channel,
	ppm,
	p_type,
	pro_state,
	pro_type,
	postal,
	loan_seq_no,
	purpose,
	l_term,
	n_of_borrowers,
	seller_name,
	service_name);
LOAD DATA CONCURRENT LOCAL INFILE 'C:/rawdata/originQ32002.txt'
    IGNORE
    INTO TABLE origin
    CHARACTER SET default
    FIELDS
        TERMINATED BY '|'
    LINES
        STARTING BY ''
        TERMINATED BY '\n'
	(score,
	fpmtdate,
	f_t,
	m_date,
	msa_md,
	mi,
	unit,
	occ,
	cltv,
	dti,
	upb,
	ltv,
	i_rate,
	channel,
	ppm,
	p_type,
	pro_state,
	pro_type,
	postal,
	loan_seq_no,
	purpose,
	l_term,
	n_of_borrowers,
	seller_name,
	service_name);
LOAD DATA CONCURRENT LOCAL INFILE 'C:/rawdata/originQ42002.txt'
    IGNORE
    INTO TABLE origin
    CHARACTER SET default
    FIELDS
        TERMINATED BY '|'
    LINES
        STARTING BY ''
        TERMINATED BY '\n'
	(score,
	fpmtdate,
	f_t,
	m_date,
	msa_md,
	mi,
	unit,
	occ,
	cltv,
	dti,
	upb,
	ltv,
	i_rate,
	channel,
	ppm,
	p_type,
	pro_state,
	pro_type,
	postal,
	loan_seq_no,
	purpose,
	l_term,
	n_of_borrowers,
	seller_name,
	service_name);
LOAD DATA CONCURRENT LOCAL INFILE 'C:/rawdata/originQ12003.txt'
    IGNORE
    INTO TABLE origin
    CHARACTER SET default
    FIELDS
        TERMINATED BY '|'
    LINES
        STARTING BY ''
        TERMINATED BY '\n'
	(score,
	fpmtdate,
	f_t,
	m_date,
	msa_md,
	mi,
	unit,
	occ,
	cltv,
	dti,
	upb,
	ltv,
	i_rate,
	channel,
	ppm,
	p_type,
	pro_state,
	pro_type,
	postal,
	loan_seq_no,
	purpose,
	l_term,
	n_of_borrowers,
	seller_name,
	service_name);
LOAD DATA CONCURRENT LOCAL INFILE 'C:/rawdata/originQ22003.txt'
    IGNORE
    INTO TABLE origin
    CHARACTER SET default
    FIELDS
        TERMINATED BY '|'
    LINES
        STARTING BY ''
        TERMINATED BY '\n'
	(score,
	fpmtdate,
	f_t,
	m_date,
	msa_md,
	mi,
	unit,
	occ,
	cltv,
	dti,
	upb,
	ltv,
	i_rate,
	channel,
	ppm,
	p_type,
	pro_state,
	pro_type,
	postal,
	loan_seq_no,
	purpose,
	l_term,
	n_of_borrowers,
	seller_name,
	service_name);
LOAD DATA CONCURRENT LOCAL INFILE 'C:/rawdata/originQ32003.txt'
    IGNORE
    INTO TABLE origin
    CHARACTER SET default
    FIELDS
        TERMINATED BY '|'
    LINES
        STARTING BY ''
        TERMINATED BY '\n'
	(score,
	fpmtdate,
	f_t,
	m_date,
	msa_md,
	mi,
	unit,
	occ,
	cltv,
	dti,
	upb,
	ltv,
	i_rate,
	channel,
	ppm,
	p_type,
	pro_state,
	pro_type,
	postal,
	loan_seq_no,
	purpose,
	l_term,
	n_of_borrowers,
	seller_name,
	service_name);
LOAD DATA CONCURRENT LOCAL INFILE 'C:/rawdata/originQ42003.txt'
    IGNORE
    INTO TABLE origin
    CHARACTER SET default
    FIELDS
        TERMINATED BY '|'
    LINES
        STARTING BY ''
        TERMINATED BY '\n'
	(score,
	fpmtdate,
	f_t,
	m_date,
	msa_md,
	mi,
	unit,
	occ,
	cltv,
	dti,
	upb,
	ltv,
	i_rate,
	channel,
	ppm,
	p_type,
	pro_state,
	pro_type,
	postal,
	loan_seq_no,
	purpose,
	l_term,
	n_of_borrowers,
	seller_name,
	service_name);
LOAD DATA CONCURRENT LOCAL INFILE 'C:/rawdata/originQ12004.txt'
    IGNORE
    INTO TABLE origin
    CHARACTER SET default
    FIELDS
        TERMINATED BY '|'
    LINES
        STARTING BY ''
        TERMINATED BY '\n'
	(score,
	fpmtdate,
	f_t,
	m_date,
	msa_md,
	mi,
	unit,
	occ,
	cltv,
	dti,
	upb,
	ltv,
	i_rate,
	channel,
	ppm,
	p_type,
	pro_state,
	pro_type,
	postal,
	loan_seq_no,
	purpose,
	l_term,
	n_of_borrowers,
	seller_name,
	service_name);
LOAD DATA CONCURRENT LOCAL INFILE 'C:/rawdata/originQ22004.txt'
    IGNORE
    INTO TABLE origin
    CHARACTER SET default
    FIELDS
        TERMINATED BY '|'
    LINES
        STARTING BY ''
        TERMINATED BY '\n'
	(score,
	fpmtdate,
	f_t,
	m_date,
	msa_md,
	mi,
	unit,
	occ,
	cltv,
	dti,
	upb,
	ltv,
	i_rate,
	channel,
	ppm,
	p_type,
	pro_state,
	pro_type,
	postal,
	loan_seq_no,
	purpose,
	l_term,
	n_of_borrowers,
	seller_name,
	service_name);
LOAD DATA CONCURRENT LOCAL INFILE 'C:/rawdata/originQ32004.txt'
    IGNORE
    INTO TABLE origin
    CHARACTER SET default
    FIELDS
        TERMINATED BY '|'
    LINES
        STARTING BY ''
        TERMINATED BY '\n'
	(score,
	fpmtdate,
	f_t,
	m_date,
	msa_md,
	mi,
	unit,
	occ,
	cltv,
	dti,
	upb,
	ltv,
	i_rate,
	channel,
	ppm,
	p_type,
	pro_state,
	pro_type,
	postal,
	loan_seq_no,
	purpose,
	l_term,
	n_of_borrowers,
	seller_name,
	service_name);
LOAD DATA CONCURRENT LOCAL INFILE 'C:/rawdata/originQ42004.txt'
    IGNORE
    INTO TABLE origin
    CHARACTER SET default
    FIELDS
        TERMINATED BY '|'
    LINES
        STARTING BY ''
        TERMINATED BY '\n'
	(score,
	fpmtdate,
	f_t,
	m_date,
	msa_md,
	mi,
	unit,
	occ,
	cltv,
	dti,
	upb,
	ltv,
	i_rate,
	channel,
	ppm,
	p_type,
	pro_state,
	pro_type,
	postal,
	loan_seq_no,
	purpose,
	l_term,
	n_of_borrowers,
	seller_name,
	service_name);

LOAD DATA CONCURRENT LOCAL INFILE 'C:/rawdata/originQ12005.txt'
    IGNORE
    INTO TABLE origin
    CHARACTER SET default
    FIELDS
        TERMINATED BY '|'
    LINES
        STARTING BY ''
        TERMINATED BY '\n'
	(score,
	fpmtdate,
	f_t,
	m_date,
	msa_md,
	mi,
	unit,
	occ,
	cltv,
	dti,
	upb,
	ltv,
	i_rate,
	channel,
	ppm,
	p_type,
	pro_state,
	pro_type,
	postal,
	loan_seq_no,
	purpose,
	l_term,
	n_of_borrowers,
	seller_name,
	service_name);
LOAD DATA CONCURRENT LOCAL INFILE 'C:/rawdata/originQ22005.txt'
    IGNORE
    INTO TABLE origin
    CHARACTER SET default
    FIELDS
        TERMINATED BY '|'
    LINES
        STARTING BY ''
        TERMINATED BY '\n'
	(score,
	fpmtdate,
	f_t,
	m_date,
	msa_md,
	mi,
	unit,
	occ,
	cltv,
	dti,
	upb,
	ltv,
	i_rate,
	channel,
	ppm,
	p_type,
	pro_state,
	pro_type,
	postal,
	loan_seq_no,
	purpose,
	l_term,
	n_of_borrowers,
	seller_name,
	service_name);
LOAD DATA CONCURRENT LOCAL INFILE 'C:/rawdata/originQ32005.txt'
    IGNORE
    INTO TABLE origin
    CHARACTER SET default
    FIELDS
        TERMINATED BY '|'
    LINES
        STARTING BY ''
        TERMINATED BY '\n'
	(score,
	fpmtdate,
	f_t,
	m_date,
	msa_md,
	mi,
	unit,
	occ,
	cltv,
	dti,
	upb,
	ltv,
	i_rate,
	channel,
	ppm,
	p_type,
	pro_state,
	pro_type,
	postal,
	loan_seq_no,
	purpose,
	l_term,
	n_of_borrowers,
	seller_name,
	service_name);
LOAD DATA CONCURRENT LOCAL INFILE 'C:/rawdata/originQ42005.txt'
    IGNORE
    INTO TABLE origin
    CHARACTER SET default
    FIELDS
        TERMINATED BY '|'
    LINES
        STARTING BY ''
        TERMINATED BY '\n'
	(score,
	fpmtdate,
	f_t,
	m_date,
	msa_md,
	mi,
	unit,
	occ,
	cltv,
	dti,
	upb,
	ltv,
	i_rate,
	channel,
	ppm,
	p_type,
	pro_state,
	pro_type,
	postal,
	loan_seq_no,
	purpose,
	l_term,
	n_of_borrowers,
	seller_name,
	service_name);
LOAD DATA CONCURRENT LOCAL INFILE 'C:/rawdata/originQ12006.txt'
    IGNORE
    INTO TABLE origin
    CHARACTER SET default
    FIELDS
        TERMINATED BY '|'
    LINES
        STARTING BY ''
        TERMINATED BY '\n'
	(score,
	fpmtdate,
	f_t,
	m_date,
	msa_md,
	mi,
	unit,
	occ,
	cltv,
	dti,
	upb,
	ltv,
	i_rate,
	channel,
	ppm,
	p_type,
	pro_state,
	pro_type,
	postal,
	loan_seq_no,
	purpose,
	l_term,
	n_of_borrowers,
	seller_name,
	service_name);
LOAD DATA CONCURRENT LOCAL INFILE 'C:/rawdata/originQ22006.txt'
    IGNORE
    INTO TABLE origin
    CHARACTER SET default
    FIELDS
        TERMINATED BY '|'
    LINES
        STARTING BY ''
        TERMINATED BY '\n'
	(score,
	fpmtdate,
	f_t,
	m_date,
	msa_md,
	mi,
	unit,
	occ,
	cltv,
	dti,
	upb,
	ltv,
	i_rate,
	channel,
	ppm,
	p_type,
	pro_state,
	pro_type,
	postal,
	loan_seq_no,
	purpose,
	l_term,
	n_of_borrowers,
	seller_name,
	service_name);
LOAD DATA CONCURRENT LOCAL INFILE 'C:/rawdata/originQ32006.txt'
    IGNORE
    INTO TABLE origin
    CHARACTER SET default
    FIELDS
        TERMINATED BY '|'
    LINES
        STARTING BY ''
        TERMINATED BY '\n'
	(score,
	fpmtdate,
	f_t,
	m_date,
	msa_md,
	mi,
	unit,
	occ,
	cltv,
	dti,
	upb,
	ltv,
	i_rate,
	channel,
	ppm,
	p_type,
	pro_state,
	pro_type,
	postal,
	loan_seq_no,
	purpose,
	l_term,
	n_of_borrowers,
	seller_name,
	service_name);
LOAD DATA CONCURRENT LOCAL INFILE 'C:/rawdata/originQ42006.txt'
    IGNORE
    INTO TABLE origin
    CHARACTER SET default
    FIELDS
        TERMINATED BY '|'
    LINES
        STARTING BY ''
        TERMINATED BY '\n'
	(score,
	fpmtdate,
	f_t,
	m_date,
	msa_md,
	mi,
	unit,
	occ,
	cltv,
	dti,
	upb,
	ltv,
	i_rate,
	channel,
	ppm,
	p_type,
	pro_state,
	pro_type,
	postal,
	loan_seq_no,
	purpose,
	l_term,
	n_of_borrowers,
	seller_name,
	service_name);
LOAD DATA CONCURRENT LOCAL INFILE 'C:/rawdata/originQ12007.txt'
    IGNORE
    INTO TABLE origin
    CHARACTER SET default
    FIELDS
        TERMINATED BY '|'
    LINES
        STARTING BY ''
        TERMINATED BY '\n'
	(score,
	fpmtdate,
	f_t,
	m_date,
	msa_md,
	mi,
	unit,
	occ,
	cltv,
	dti,
	upb,
	ltv,
	i_rate,
	channel,
	ppm,
	p_type,
	pro_state,
	pro_type,
	postal,
	loan_seq_no,
	purpose,
	l_term,
	n_of_borrowers,
	seller_name,
	service_name);
LOAD DATA CONCURRENT LOCAL INFILE 'C:/rawdata/originQ22007.txt'
    IGNORE
    INTO TABLE origin
    CHARACTER SET default
    FIELDS
        TERMINATED BY '|'
    LINES
        STARTING BY ''
        TERMINATED BY '\n'
	(score,
	fpmtdate,
	f_t,
	m_date,
	msa_md,
	mi,
	unit,
	occ,
	cltv,
	dti,
	upb,
	ltv,
	i_rate,
	channel,
	ppm,
	p_type,
	pro_state,
	pro_type,
	postal,
	loan_seq_no,
	purpose,
	l_term,
	n_of_borrowers,
	seller_name,
	service_name);
LOAD DATA CONCURRENT LOCAL INFILE 'C:/rawdata/originQ32007.txt'
    IGNORE
    INTO TABLE origin
    CHARACTER SET default
    FIELDS
        TERMINATED BY '|'
    LINES
        STARTING BY ''
        TERMINATED BY '\n'
	(score,
	fpmtdate,
	f_t,
	m_date,
	msa_md,
	mi,
	unit,
	occ,
	cltv,
	dti,
	upb,
	ltv,
	i_rate,
	channel,
	ppm,
	p_type,
	pro_state,
	pro_type,
	postal,
	loan_seq_no,
	purpose,
	l_term,
	n_of_borrowers,
	seller_name,
	service_name);
LOAD DATA CONCURRENT LOCAL INFILE 'C:/rawdata/originQ42007.txt'
    IGNORE
    INTO TABLE origin
    CHARACTER SET default
    FIELDS
        TERMINATED BY '|'
    LINES
        STARTING BY ''
        TERMINATED BY '\n'
	(score,
	fpmtdate,
	f_t,
	m_date,
	msa_md,
	mi,
	unit,
	occ,
	cltv,
	dti,
	upb,
	ltv,
	i_rate,
	channel,
	ppm,
	p_type,
	pro_state,
	pro_type,
	postal,
	loan_seq_no,
	purpose,
	l_term,
	n_of_borrowers,
	seller_name,
	service_name);
LOAD DATA CONCURRENT LOCAL INFILE 'C:/rawdata/originQ12008.txt'
    IGNORE
    INTO TABLE origin
    CHARACTER SET default
    FIELDS
        TERMINATED BY '|'
    LINES
        STARTING BY ''
        TERMINATED BY '\n'
	(score,
	fpmtdate,
	f_t,
	m_date,
	msa_md,
	mi,
	unit,
	occ,
	cltv,
	dti,
	upb,
	ltv,
	i_rate,
	channel,
	ppm,
	p_type,
	pro_state,
	pro_type,
	postal,
	loan_seq_no,
	purpose,
	l_term,
	n_of_borrowers,
	seller_name,
	service_name);
LOAD DATA CONCURRENT LOCAL INFILE 'C:/rawdata/originQ22008.txt'
    IGNORE
    INTO TABLE origin
    CHARACTER SET default
    FIELDS
        TERMINATED BY '|'
    LINES
        STARTING BY ''
        TERMINATED BY '\n'
	(score,
	fpmtdate,
	f_t,
	m_date,
	msa_md,
	mi,
	unit,
	occ,
	cltv,
	dti,
	upb,
	ltv,
	i_rate,
	channel,
	ppm,
	p_type,
	pro_state,
	pro_type,
	postal,
	loan_seq_no,
	purpose,
	l_term,
	n_of_borrowers,
	seller_name,
	service_name);
LOAD DATA CONCURRENT LOCAL INFILE 'C:/rawdata/originQ32008.txt'
    IGNORE
    INTO TABLE origin
    CHARACTER SET default
    FIELDS
        TERMINATED BY '|'
    LINES
        STARTING BY ''
        TERMINATED BY '\n'
	(score,
	fpmtdate,
	f_t,
	m_date,
	msa_md,
	mi,
	unit,
	occ,
	cltv,
	dti,
	upb,
	ltv,
	i_rate,
	channel,
	ppm,
	p_type,
	pro_state,
	pro_type,
	postal,
	loan_seq_no,
	purpose,
	l_term,
	n_of_borrowers,
	seller_name,
	service_name);
LOAD DATA CONCURRENT LOCAL INFILE 'C:/rawdata/originQ42008.txt'
    IGNORE
    INTO TABLE origin
    CHARACTER SET default
    FIELDS
        TERMINATED BY '|'
    LINES
        STARTING BY ''
        TERMINATED BY '\n'
	(score,
	fpmtdate,
	f_t,
	m_date,
	msa_md,
	mi,
	unit,
	occ,
	cltv,
	dti,
	upb,
	ltv,
	i_rate,
	channel,
	ppm,
	p_type,
	pro_state,
	pro_type,
	postal,
	loan_seq_no,
	purpose,
	l_term,
	n_of_borrowers,
	seller_name,
	service_name);
LOAD DATA CONCURRENT LOCAL INFILE 'C:/rawdata/originQ12009.txt'
    IGNORE
    INTO TABLE origin
    CHARACTER SET default
    FIELDS
        TERMINATED BY '|'
    LINES
        STARTING BY ''
        TERMINATED BY '\n'
	(score,
	fpmtdate,
	f_t,
	m_date,
	msa_md,
	mi,
	unit,
	occ,
	cltv,
	dti,
	upb,
	ltv,
	i_rate,
	channel,
	ppm,
	p_type,
	pro_state,
	pro_type,
	postal,
	loan_seq_no,
	purpose,
	l_term,
	n_of_borrowers,
	seller_name,
	service_name);
LOAD DATA CONCURRENT LOCAL INFILE 'C:/rawdata/originQ22009.txt'
    IGNORE
    INTO TABLE origin
    CHARACTER SET default
    FIELDS
        TERMINATED BY '|'
    LINES
        STARTING BY ''
        TERMINATED BY '\n'
	(score,
	fpmtdate,
	f_t,
	m_date,
	msa_md,
	mi,
	unit,
	occ,
	cltv,
	dti,
	upb,
	ltv,
	i_rate,
	channel,
	ppm,
	p_type,
	pro_state,
	pro_type,
	postal,
	loan_seq_no,
	purpose,
	l_term,
	n_of_borrowers,
	seller_name,
	service_name);

LOAD DATA CONCURRENT LOCAL INFILE 'C:/rawdata/originQ32009.txt'
    IGNORE
    INTO TABLE origin
    CHARACTER SET default
    FIELDS
        TERMINATED BY '|'
    LINES
        STARTING BY ''
        TERMINATED BY '\n'
	(score,
	fpmtdate,
	f_t,
	m_date,
	msa_md,
	mi,
	unit,
	occ,
	cltv,
	dti,
	upb,
	ltv,
	i_rate,
	channel,
	ppm,
	p_type,
	pro_state,
	pro_type,
	postal,
	loan_seq_no,
	purpose,
	l_term,
	n_of_borrowers,
	seller_name,
	service_name);
LOAD DATA CONCURRENT LOCAL INFILE 'C:/rawdata/originQ42009.txt'
    IGNORE
    INTO TABLE origin
    CHARACTER SET default
    FIELDS
        TERMINATED BY '|'
    LINES
        STARTING BY ''
        TERMINATED BY '\n'
	(score,
	fpmtdate,
	f_t,
	m_date,
	msa_md,
	mi,
	unit,
	occ,
	cltv,
	dti,
	upb,
	ltv,
	i_rate,
	channel,
	ppm,
	p_type,
	pro_state,
	pro_type,
	postal,
	loan_seq_no,
	purpose,
	l_term,
	n_of_borrowers,
	seller_name,
	service_name);
LOAD DATA CONCURRENT LOCAL INFILE 'C:/rawdata/originQ12010.txt'
    IGNORE
    INTO TABLE origin
    CHARACTER SET default
    FIELDS
        TERMINATED BY '|'
    LINES
        STARTING BY ''
        TERMINATED BY '\n'
	(score,
	fpmtdate,
	f_t,
	m_date,
	msa_md,
	mi,
	unit,
	occ,
	cltv,
	dti,
	upb,
	ltv,
	i_rate,
	channel,
	ppm,
	p_type,
	pro_state,
	pro_type,
	postal,
	loan_seq_no,
	purpose,
	l_term,
	n_of_borrowers,
	seller_name,
	service_name);
LOAD DATA CONCURRENT LOCAL INFILE 'C:/rawdata/originQ22010.txt'
    IGNORE
    INTO TABLE origin
    CHARACTER SET default
    FIELDS
        TERMINATED BY '|'
    LINES
        STARTING BY ''
        TERMINATED BY '\n'
	(score,
	fpmtdate,
	f_t,
	m_date,
	msa_md,
	mi,
	unit,
	occ,
	cltv,
	dti,
	upb,
	ltv,
	i_rate,
	channel,
	ppm,
	p_type,
	pro_state,
	pro_type,
	postal,
	loan_seq_no,
	purpose,
	l_term,
	n_of_borrowers,
	seller_name,
	service_name);
LOAD DATA CONCURRENT LOCAL INFILE 'C:/rawdata/originQ32010.txt'
    IGNORE
    INTO TABLE origin
    CHARACTER SET default
    FIELDS
        TERMINATED BY '|'
    LINES
        STARTING BY ''
        TERMINATED BY '\n'
	(score,
	fpmtdate,
	f_t,
	m_date,
	msa_md,
	mi,
	unit,
	occ,
	cltv,
	dti,
	upb,
	ltv,
	i_rate,
	channel,
	ppm,
	p_type,
	pro_state,
	pro_type,
	postal,
	loan_seq_no,
	purpose,
	l_term,
	n_of_borrowers,
	seller_name,
	service_name);
LOAD DATA CONCURRENT LOCAL INFILE 'C:/rawdata/originQ42010.txt'
    IGNORE
    INTO TABLE origin
    CHARACTER SET default
    FIELDS
        TERMINATED BY '|'
    LINES
        STARTING BY ''
        TERMINATED BY '\n'
	(score,
	fpmtdate,
	f_t,
	m_date,
	msa_md,
	mi,
	unit,
	occ,
	cltv,
	dti,
	upb,
	ltv,
	i_rate,
	channel,
	ppm,
	p_type,
	pro_state,
	pro_type,
	postal,
	loan_seq_no,
	purpose,
	l_term,
	n_of_borrowers,
	seller_name,
	service_name);
LOAD DATA CONCURRENT LOCAL INFILE 'C:/rawdata/originQ12011.txt'
    IGNORE
    INTO TABLE origin
    CHARACTER SET default
    FIELDS
        TERMINATED BY '|'
    LINES
        STARTING BY ''
        TERMINATED BY '\n'
	(score,
	fpmtdate,
	f_t,
	m_date,
	msa_md,
	mi,
	unit,
	occ,
	cltv,
	dti,
	upb,
	ltv,
	i_rate,
	channel,
	ppm,
	p_type,
	pro_state,
	pro_type,
	postal,
	loan_seq_no,
	purpose,
	l_term,
	n_of_borrowers,
	seller_name,
	service_name);
LOAD DATA CONCURRENT LOCAL INFILE 'C:/rawdata/originQ22011.txt'
    IGNORE
    INTO TABLE origin
    CHARACTER SET default
    FIELDS
        TERMINATED BY '|'
    LINES
        STARTING BY ''
        TERMINATED BY '\n'
	(score,
	fpmtdate,
	f_t,
	m_date,
	msa_md,
	mi,
	unit,
	occ,
	cltv,
	dti,
	upb,
	ltv,
	i_rate,
	channel,
	ppm,
	p_type,
	pro_state,
	pro_type,
	postal,
	loan_seq_no,
	purpose,
	l_term,
	n_of_borrowers,
	seller_name,
	service_name);
LOAD DATA CONCURRENT LOCAL INFILE 'C:/rawdata/originQ32011.txt'
    IGNORE
    INTO TABLE origin
    CHARACTER SET default
    FIELDS
        TERMINATED BY '|'
    LINES
        STARTING BY ''
        TERMINATED BY '\n'
	(score,
	fpmtdate,
	f_t,
	m_date,
	msa_md,
	mi,
	unit,
	occ,
	cltv,
	dti,
	upb,
	ltv,
	i_rate,
	channel,
	ppm,
	p_type,
	pro_state,
	pro_type,
	postal,
	loan_seq_no,
	purpose,
	l_term,
	n_of_borrowers,
	seller_name,
	service_name);
LOAD DATA CONCURRENT LOCAL INFILE 'C:/rawdata/originQ42011.txt'
    IGNORE
    INTO TABLE origin
    CHARACTER SET default
    FIELDS
        TERMINATED BY '|'
    LINES
        STARTING BY ''
        TERMINATED BY '\n'
	(score,
	fpmtdate,
	f_t,
	m_date,
	msa_md,
	mi,
	unit,
	occ,
	cltv,
	dti,
	upb,
	ltv,
	i_rate,
	channel,
	ppm,
	p_type,
	pro_state,
	pro_type,
	postal,
	loan_seq_no,
	purpose,
	l_term,
	n_of_borrowers,
	seller_name,
	service_name);
LOAD DATA CONCURRENT LOCAL INFILE 'C:/rawdata/originQ12012.txt'
    IGNORE
    INTO TABLE origin
    CHARACTER SET default
    FIELDS
        TERMINATED BY '|'
    LINES
        STARTING BY ''
        TERMINATED BY '\n'
	(score,
	fpmtdate,
	f_t,
	m_date,
	msa_md,
	mi,
	unit,
	occ,
	cltv,
	dti,
	upb,
	ltv,
	i_rate,
	channel,
	ppm,
	p_type,
	pro_state,
	pro_type,
	postal,
	loan_seq_no,
	purpose,
	l_term,
	n_of_borrowers,
	seller_name,
	service_name);
LOAD DATA CONCURRENT LOCAL INFILE 'C:/rawdata/originQ22012.txt'
    IGNORE
    INTO TABLE origin
    CHARACTER SET default
    FIELDS
        TERMINATED BY '|'
    LINES
        STARTING BY ''
        TERMINATED BY '\n'
	(score,
	fpmtdate,
	f_t,
	m_date,
	msa_md,
	mi,
	unit,
	occ,
	cltv,
	dti,
	upb,
	ltv,
	i_rate,
	channel,
	ppm,
	p_type,
	pro_state,
	pro_type,
	postal,
	loan_seq_no,
	purpose,
	l_term,
	n_of_borrowers,
	seller_name,
	service_name);
LOAD DATA CONCURRENT LOCAL INFILE 'C:/rawdata/originQ32012.txt'
    IGNORE
    INTO TABLE origin
    CHARACTER SET default
    FIELDS
        TERMINATED BY '|'
    LINES
        STARTING BY ''
        TERMINATED BY '\n'
	(score,
	fpmtdate,
	f_t,
	m_date,
	msa_md,
	mi,
	unit,
	occ,
	cltv,
	dti,
	upb,
	ltv,
	i_rate,
	channel,
	ppm,
	p_type,
	pro_state,
	pro_type,
	postal,
	loan_seq_no,
	purpose,
	l_term,
	n_of_borrowers,
	seller_name,
	service_name);
LOAD DATA CONCURRENT LOCAL INFILE 'C:/rawdata/originQ42012.txt'
    IGNORE
    INTO TABLE origin
    CHARACTER SET default
    FIELDS
        TERMINATED BY '|'
    LINES
        STARTING BY ''
        TERMINATED BY '\n'
	(score,
	fpmtdate,
	f_t,
	m_date,
	msa_md,
	mi,
	unit,
	occ,
	cltv,
	dti,
	upb,
	ltv,
	i_rate,
	channel,
	ppm,
	p_type,
	pro_state,
	pro_type,
	postal,
	loan_seq_no,
	purpose,
	l_term,
	n_of_borrowers,
	seller_name,
	service_name);
LOAD DATA CONCURRENT LOCAL INFILE 'C:/rawdata/originQ12013.txt'
    IGNORE
    INTO TABLE origin
    CHARACTER SET default
    FIELDS
        TERMINATED BY '|'
    LINES
        STARTING BY ''
        TERMINATED BY '\n'
	(score,
	fpmtdate,
	f_t,
	m_date,
	msa_md,
	mi,
	unit,
	occ,
	cltv,
	dti,
	upb,
	ltv,
	i_rate,
	channel,
	ppm,
	p_type,
	pro_state,
	pro_type,
	postal,
	loan_seq_no,
	purpose,
	l_term,
	n_of_borrowers,
	seller_name,
	service_name);
LOAD DATA CONCURRENT LOCAL INFILE 'C:/rawdata/originQ22013.txt'
    IGNORE
    INTO TABLE origin
    CHARACTER SET default
    FIELDS
        TERMINATED BY '|'
    LINES
        STARTING BY ''
        TERMINATED BY '\n'
	(score,
	fpmtdate,
	f_t,
	m_date,
	msa_md,
	mi,
	unit,
	occ,
	cltv,
	dti,
	upb,
	ltv,
	i_rate,
	channel,
	ppm,
	p_type,
	pro_state,
	pro_type,
	postal,
	loan_seq_no,
	purpose,
	l_term,
	n_of_borrowers,
	seller_name,
	service_name);
