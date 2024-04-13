--
-- PostgreSQL database dump
--

-- Dumped from database version 15.2
-- Dumped by pg_dump version 15.2

-- Started on 2024-04-13 13:18:30 IST

SET statement_timeout = 0;
SET lock_timeout = 0;
SET idle_in_transaction_session_timeout = 0;
SET client_encoding = 'UTF8';
SET standard_conforming_strings = on;
SELECT pg_catalog.set_config('search_path', '', false);
SET check_function_bodies = false;
SET xmloption = content;
SET client_min_messages = warning;
SET row_security = off;

SET default_tablespace = '';

SET default_table_access_method = heap;

--
-- TOC entry 217 (class 1259 OID 17564)
-- Name: admininfo; Type: TABLE; Schema: public; Owner: postgres
--

CREATE TABLE public.admininfo (
    admin_id integer NOT NULL,
    passwd character varying(20),
    role character varying(20),
    user_id integer NOT NULL
);


ALTER TABLE public.admininfo OWNER TO postgres;

--
-- TOC entry 219 (class 1259 OID 17579)
-- Name: airlineinfo; Type: TABLE; Schema: public; Owner: postgres
--

CREATE TABLE public.airlineinfo (
    airline_name character varying(20) NOT NULL,
    flight_id character varying(10) NOT NULL
);


ALTER TABLE public.airlineinfo OWNER TO postgres;

--
-- TOC entry 222 (class 1259 OID 17609)
-- Name: bookinginfo; Type: TABLE; Schema: public; Owner: postgres
--

CREATE TABLE public.bookinginfo (
    booking_id character varying(10) NOT NULL,
    customer_id character varying(10) NOT NULL,
    dep_date date,
    arrival_time date
);


ALTER TABLE public.bookinginfo OWNER TO postgres;

--
-- TOC entry 216 (class 1259 OID 17554)
-- Name: customerinfo; Type: TABLE; Schema: public; Owner: postgres
--

CREATE TABLE public.customerinfo (
    customer_id character varying(10) NOT NULL,
    user_id integer NOT NULL
);


ALTER TABLE public.customerinfo OWNER TO postgres;

--
-- TOC entry 218 (class 1259 OID 17574)
-- Name: flightinfo; Type: TABLE; Schema: public; Owner: postgres
--

CREATE TABLE public.flightinfo (
    flight_id character varying(10) NOT NULL,
    dep_location character varying(20),
    arrival_location character varying(20),
    dep_time time without time zone,
    arr_time time without time zone
);


ALTER TABLE public.flightinfo OWNER TO postgres;

--
-- TOC entry 215 (class 1259 OID 17544)
-- Name: passengerinfo; Type: TABLE; Schema: public; Owner: postgres
--

CREATE TABLE public.passengerinfo (
    passenger_id character varying(20) NOT NULL,
    user_id integer NOT NULL
);


ALTER TABLE public.passengerinfo OWNER TO postgres;

--
-- TOC entry 224 (class 1259 OID 17639)
-- Name: payments; Type: TABLE; Schema: public; Owner: postgres
--

CREATE TABLE public.payments (
    payment_id character varying(10) NOT NULL,
    booking_id character varying(10) NOT NULL,
    amount real
);


ALTER TABLE public.payments OWNER TO postgres;

--
-- TOC entry 221 (class 1259 OID 17594)
-- Name: seatflight; Type: TABLE; Schema: public; Owner: postgres
--

CREATE TABLE public.seatflight (
    seat_id character varying(5) NOT NULL,
    flight_id character varying(10) NOT NULL
);


ALTER TABLE public.seatflight OWNER TO postgres;

--
-- TOC entry 220 (class 1259 OID 17589)
-- Name: seatinfo; Type: TABLE; Schema: public; Owner: postgres
--

CREATE TABLE public.seatinfo (
    seat_id character varying(5) NOT NULL,
    preference character varying(10),
    price real
);


ALTER TABLE public.seatinfo OWNER TO postgres;

--
-- TOC entry 223 (class 1259 OID 17619)
-- Name: seatsbooked; Type: TABLE; Schema: public; Owner: postgres
--

CREATE TABLE public.seatsbooked (
    booking_id character varying(10) NOT NULL,
    seat_id character varying(5) NOT NULL,
    flight_id character varying(10) NOT NULL,
    passenger_id character varying(10)
);


ALTER TABLE public.seatsbooked OWNER TO postgres;

--
-- TOC entry 214 (class 1259 OID 17529)
-- Name: users; Type: TABLE; Schema: public; Owner: postgres
--

CREATE TABLE public.users (
    user_id integer NOT NULL,
    passwd character varying(20),
    firstname character varying(20),
    lastname character varying(20),
    phoneno character varying(15),
    email character varying(40)
);


ALTER TABLE public.users OWNER TO postgres;

--
-- TOC entry 3485 (class 2606 OID 17568)
-- Name: admininfo admininfo_pkey; Type: CONSTRAINT; Schema: public; Owner: postgres
--

ALTER TABLE ONLY public.admininfo
    ADD CONSTRAINT admininfo_pkey PRIMARY KEY (admin_id);


--
-- TOC entry 3489 (class 2606 OID 17583)
-- Name: airlineinfo airlineinfo_pkey; Type: CONSTRAINT; Schema: public; Owner: postgres
--

ALTER TABLE ONLY public.airlineinfo
    ADD CONSTRAINT airlineinfo_pkey PRIMARY KEY (airline_name, flight_id);


--
-- TOC entry 3495 (class 2606 OID 17613)
-- Name: bookinginfo bookinginfo_pkey; Type: CONSTRAINT; Schema: public; Owner: postgres
--

ALTER TABLE ONLY public.bookinginfo
    ADD CONSTRAINT bookinginfo_pkey PRIMARY KEY (booking_id);


--
-- TOC entry 3483 (class 2606 OID 17558)
-- Name: customerinfo customerinfo_pkey; Type: CONSTRAINT; Schema: public; Owner: postgres
--

ALTER TABLE ONLY public.customerinfo
    ADD CONSTRAINT customerinfo_pkey PRIMARY KEY (customer_id);


--
-- TOC entry 3487 (class 2606 OID 17578)
-- Name: flightinfo flightinfo_pkey; Type: CONSTRAINT; Schema: public; Owner: postgres
--

ALTER TABLE ONLY public.flightinfo
    ADD CONSTRAINT flightinfo_pkey PRIMARY KEY (flight_id);


--
-- TOC entry 3481 (class 2606 OID 17548)
-- Name: passengerinfo passengerinfo_pkey; Type: CONSTRAINT; Schema: public; Owner: postgres
--

ALTER TABLE ONLY public.passengerinfo
    ADD CONSTRAINT passengerinfo_pkey PRIMARY KEY (passenger_id);


--
-- TOC entry 3499 (class 2606 OID 17643)
-- Name: payments payments_pkey; Type: CONSTRAINT; Schema: public; Owner: postgres
--

ALTER TABLE ONLY public.payments
    ADD CONSTRAINT payments_pkey PRIMARY KEY (payment_id);


--
-- TOC entry 3493 (class 2606 OID 17598)
-- Name: seatflight seatflight_pkey; Type: CONSTRAINT; Schema: public; Owner: postgres
--

ALTER TABLE ONLY public.seatflight
    ADD CONSTRAINT seatflight_pkey PRIMARY KEY (seat_id, flight_id);


--
-- TOC entry 3491 (class 2606 OID 17593)
-- Name: seatinfo seatinfo_pkey; Type: CONSTRAINT; Schema: public; Owner: postgres
--

ALTER TABLE ONLY public.seatinfo
    ADD CONSTRAINT seatinfo_pkey PRIMARY KEY (seat_id);


--
-- TOC entry 3497 (class 2606 OID 17623)
-- Name: seatsbooked seatsbooked_pkey; Type: CONSTRAINT; Schema: public; Owner: postgres
--

ALTER TABLE ONLY public.seatsbooked
    ADD CONSTRAINT seatsbooked_pkey PRIMARY KEY (booking_id, seat_id, flight_id);


--
-- TOC entry 3479 (class 2606 OID 17533)
-- Name: users users_pkey; Type: CONSTRAINT; Schema: public; Owner: postgres
--

ALTER TABLE ONLY public.users
    ADD CONSTRAINT users_pkey PRIMARY KEY (user_id);


--
-- TOC entry 3507 (class 2606 OID 17624)
-- Name: seatsbooked booking_id; Type: FK CONSTRAINT; Schema: public; Owner: postgres
--

ALTER TABLE ONLY public.seatsbooked
    ADD CONSTRAINT booking_id FOREIGN KEY (booking_id) REFERENCES public.bookinginfo(booking_id);


--
-- TOC entry 3510 (class 2606 OID 17644)
-- Name: payments booking_id; Type: FK CONSTRAINT; Schema: public; Owner: postgres
--

ALTER TABLE ONLY public.payments
    ADD CONSTRAINT booking_id FOREIGN KEY (booking_id) REFERENCES public.bookinginfo(booking_id);


--
-- TOC entry 3506 (class 2606 OID 17614)
-- Name: bookinginfo customer_id; Type: FK CONSTRAINT; Schema: public; Owner: postgres
--

ALTER TABLE ONLY public.bookinginfo
    ADD CONSTRAINT customer_id FOREIGN KEY (customer_id) REFERENCES public.customerinfo(customer_id);


--
-- TOC entry 3503 (class 2606 OID 17584)
-- Name: airlineinfo flight_id; Type: FK CONSTRAINT; Schema: public; Owner: postgres
--

ALTER TABLE ONLY public.airlineinfo
    ADD CONSTRAINT flight_id FOREIGN KEY (flight_id) REFERENCES public.flightinfo(flight_id);


--
-- TOC entry 3504 (class 2606 OID 17604)
-- Name: seatflight flight_id; Type: FK CONSTRAINT; Schema: public; Owner: postgres
--

ALTER TABLE ONLY public.seatflight
    ADD CONSTRAINT flight_id FOREIGN KEY (flight_id) REFERENCES public.flightinfo(flight_id);


--
-- TOC entry 3508 (class 2606 OID 17634)
-- Name: seatsbooked flight_id; Type: FK CONSTRAINT; Schema: public; Owner: postgres
--

ALTER TABLE ONLY public.seatsbooked
    ADD CONSTRAINT flight_id FOREIGN KEY (flight_id) REFERENCES public.flightinfo(flight_id);


--
-- TOC entry 3505 (class 2606 OID 17599)
-- Name: seatflight seat_id; Type: FK CONSTRAINT; Schema: public; Owner: postgres
--

ALTER TABLE ONLY public.seatflight
    ADD CONSTRAINT seat_id FOREIGN KEY (seat_id) REFERENCES public.seatinfo(seat_id);


--
-- TOC entry 3509 (class 2606 OID 17629)
-- Name: seatsbooked seat_id; Type: FK CONSTRAINT; Schema: public; Owner: postgres
--

ALTER TABLE ONLY public.seatsbooked
    ADD CONSTRAINT seat_id FOREIGN KEY (seat_id) REFERENCES public.seatinfo(seat_id);


--
-- TOC entry 3500 (class 2606 OID 17549)
-- Name: passengerinfo user_id; Type: FK CONSTRAINT; Schema: public; Owner: postgres
--

ALTER TABLE ONLY public.passengerinfo
    ADD CONSTRAINT user_id FOREIGN KEY (user_id) REFERENCES public.users(user_id);


--
-- TOC entry 3501 (class 2606 OID 17559)
-- Name: customerinfo user_id; Type: FK CONSTRAINT; Schema: public; Owner: postgres
--

ALTER TABLE ONLY public.customerinfo
    ADD CONSTRAINT user_id FOREIGN KEY (user_id) REFERENCES public.users(user_id);


--
-- TOC entry 3502 (class 2606 OID 17569)
-- Name: admininfo user_id; Type: FK CONSTRAINT; Schema: public; Owner: postgres
--

ALTER TABLE ONLY public.admininfo
    ADD CONSTRAINT user_id FOREIGN KEY (user_id) REFERENCES public.users(user_id);


-- Completed on 2024-04-13 13:18:30 IST

--
-- PostgreSQL database dump complete
--

